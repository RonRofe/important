# Important things // Angular

## Terminal Commands

### Installing Angular CLI
Installing Angular CLI globally on the machine: `npm install -g @angular/cli`  
*In MAC - add "sudo" at the beginning of the command.*

### New Angular Project
Generating new Angular project folder with all the dependencies: `ng new PROJECT_NAME`  
*Project name can not be `test` or starting with a number*

### Running Angular Server
Running Angular server on port `4200`: `ng serve`  
Server URL: `localhost:4200`

### Installing Angular Material
Installing Angular Material locally in the project: `ng add @angular/material`

### Generating Component
Generate a new component to the project by the CLI: `ng g c COMPONENT_PATH_AND_NAME --skipTests`  
*Remove `--skipTests` if interested in the spec file*

### Deployment
Prepare all front-end files for deploying the app: `ng build --prod`  
Destination folder can be set under `angular.json` file -> `outputPath`. 

### Check For Updates Of Angular Dependencies
Run the following to analyse non updated packages: `ng update`.

## Pipes

### Add Pipe
1. Create file with the following format: `FILE_NAME.pipe.ts`
2. File content:  
**PIPE_NAME**: The string which will be used to activate the pipe. *Lower case letters only*.  
**PIPE_CLASS**: Similar to PIPE_NAME, *first letter upper case*.  
**PARAMETERS**: Define parameters to custom pipe on use.  
**NEW_VALUE**: The value to transform to.
```typescript
import { PipeTransform, Pipe } from '@angular/core';

@Pipe({
    name: '[PIPE_NAME]'
})
export class [PIPE_CLASS]Pipe implements PipeTransform {
    transform([PARAMETERS]]) {
        return [NEW_VALUE];
    }
}
```
3. Import the class into `app.module.ts` file and use it in `delcarations:` array.

## NgModule

## imports & exports shortcut

Instead of importing and exporting the same module in `NgModule`, we can use the shortcut - use `exports:` only.  

**Example:**
```typescript
    @NgModule({
        imports: [
        MatInputModule
        ],
        exports: [
            MatIpnutModule
        ]
    })
    export class AngularMaterialModule {}
```
Replace with:
```typescript
    @NgModule({
        exports: [
            MatIpnutModule
        ]
    })
    export class AngularMaterialModule {}
```
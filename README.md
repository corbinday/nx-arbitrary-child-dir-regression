This is a basic nx workspace generated with `npx create-nx-workspace` (I selected `integrated` and `apps` and declined distributed caching).
It contains two react apps generated via `nx g @nrwl/react:app app-name`.

According to Nrwl, `nx` commands should work anywhere in the workspace, but that is not what I was finding as of nx v15.7.1

When I navigate to the docker-compose folder or any other subfolder and run `nx run-many --target=build`, the command fails with this error:

    >  NX   Could not resolve entry module "apps/app1/index.html".

I didn't test all the commands, but `nx run-many` only seems to work in the workspace root folder.

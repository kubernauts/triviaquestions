#Topic - What all changes can be applied to a running pod and those you cannot apply, what are two alternative ways to apply them?
Answer - If you need to update the fields that are not editable you do a kubectl edit and save though the changes are not applied but a new yaml is saved at a tmp location . Now delete that pad and recreate from the tmp generated yaml.  
Another way is have that pod yaml exported with -o yaml then edit and then create.

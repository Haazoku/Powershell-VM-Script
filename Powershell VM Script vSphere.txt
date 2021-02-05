$VMCreatorInput = [System.Windows.MessageBox]::Show('Do you want to create a new VM?','VM Creator','YesNo','Error')

switch ($VMCreatorInput) {

'Yes' {

#Connecting to the server
connect-viserver SERVER_IP -user USERNAME -password PASSWORD

#Template = TemplateName
$template=get-template TEMPLATE_NAME
$vmhost=get-vmhost 192.168.40.11
$datastore=get-datastore Datastore_11

#VMName = New VMName
$vmname="VM_NAME"

new-vm -name $vmname -datastore $datastore -vmhost $vmhost -template $template -RunAsync -confirm:$false

}

'No' {

#Add something else here if you want...

}

}
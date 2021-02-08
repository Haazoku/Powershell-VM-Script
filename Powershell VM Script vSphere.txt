$VMCreatorInput = [System.Windows.MessageBox]::Show('Do you want to create a new VM?','VM Creator','YesNo','Error')

switch ($VMCreatorInput) {

'Yes' {

#Change VM_NAME
$vmname="VM_NAME"

#Change SERVER_IP, USERNAME, and PASSWORD
connect-viserver SERVER_IP -user USERNAME -password PASSWORD

#Change TEMPLATE_NAME, SERVER_IP, and DATASTORE_NAME
$template=get-template TEMPLATE_NAME
$vmhost=get-vmhost SERVER_IP
$datastore=get-datastore DATASTORE_NAME


new-vm -name $vmname -datastore $datastore -vmhost $vmhost -template $template -RunAsync -confirm:$false

}

'No' {

#Add something else here if you want...

}

}

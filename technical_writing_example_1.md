# Enabling Stylized Local PDF Output in oXygen
The purpose of these instructions is to help you configure oXygen to enable local PDF preview for individual topics.
1. Copy `pluginExample` plugin from your DITA-OT directory.
1. Paste the plugin to your local DITA-OT directory. Directory found from oXygen files.
`C:\Program Files\Oxygen XML Author\frameworks\dita\DITA-OTx.x\plugins`
1. Open the XML file you want to preview in oXygen.
1. Click **Configure transformation scenarios** -> **New** -> **DITA-OT transformation** -> **pdf**
> **NOTE:** If **pdf** is not visible as a DITA-OT transformation, restart oXygen.
1. Change the DITA Scenario name to something easily identifiable, for example, *pdf2*.
1. Configure **Parameters**:
    - `dita.dir`: Change the location to your DITA-OT directory.
    - `transtype`: Insert value `pdf2`.
1. Configure **Output**:
    - **Temporary files directory** and **Output directory**: Change the default directory to a location from where the files are easily accessible, for example desktop or a designated folder on your local hard drive.
> **NOTE:** Default setting is the XML file source folder, which often is in a Git/SVN repository. Changing the directory to a local folder prevents generating unnecessary files to the Git/SVN repository.
1. Click **OK**.
1. Click **Apply associated**.
> **NOTE:** The transformation scenario does not complete if there are fig elements with an image within the topic. The transformation scenario can be completed by removing the fig elements and inserting the image separately into the topic. Remember to restore the fig elements once you have previewed the topic and you are ready to commit the changes.
oXygen completes the transformation scenario and a stylized PDF is now viewable.
Once you have completed the preview, delete the files created by the transformation scenario from the previously set location in **Temporary files directory** and **Output directory**. 
> **NOTE:** Variables and conditions do not function in the PDF output unless they are separately configured.
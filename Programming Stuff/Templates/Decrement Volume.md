<%*
const file = app.workspace.getActiveFile();
if (file) {
    await app.fileManager.processFrontMatter(file, (fm) => {
        fm.volumes_read = Math.max(0, (Number(fm.volumes_read) || 0) - 1);
    });
}
tR = "";
%>
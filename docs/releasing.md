# Releasing

* Update the version number in `build.ini`.
* Run `phing set-version`.
* Pun `phing` to make the new package for the version.
* Run `phing tag`.
* Push the commits and tags up to Github.
* Go to the releases page on Github.
* Click on the new tag.
  - Click the `Edit Tag` button.
  - Fill in the title and description for the release.
  - Attach the zip-file for the package to the release. Wait for the file to complete uploading!
  - Click the `Publish Release` button.
* Create a new `<update>` tag in the `manifest.xml` file.
  - Change the `<version>` tag to the new version.
  - Change the `<downloadurl>` tag to match the URL of the new release.
  - Commit the change.

## Trouble shooting

* The update site can become disabled if it can't be contacted.
* Packages must include the `<client>site</client>` otherwise they default to client_id = 1.

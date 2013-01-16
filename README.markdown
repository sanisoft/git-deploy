# Git Deploy Phing Script

Phing script to export the files that changed since most recent tag, upload them via FTP or SCP, and adding new tag.

Purpose of this script is to simplify deployment process for actively developing projects. It is assumed that your live app resembles with master branch and you are creating tags after each deploy.

## How to use

**Normal Uploading**

1. phing creatediff
2. phing ftpupload OR phing scpupload
3. phing createtag

**SAFE Uploading**

1. phing creatediff
2. phing safeftpupload OR phing safescpupload
3. phing safeupgrade
4. phing safedowngrade (for rollbacking changes if something goes wrong)
5. phing saferemovebackups (will remove all temporary/backup folders on server)
6. phing createtag


## Authors

**Rakesh Tembhurne**

+ http://twitter.com/tembhurnerakesh
+ http://github.com/rakeshtembhurne


## Copyright and license

Copyright 2013 [SANIsoft Technologies](http://sanisoft.com/)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
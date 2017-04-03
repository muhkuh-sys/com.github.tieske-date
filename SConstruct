# -*- coding: utf-8 -*-
#-------------------------------------------------------------------------#
#   Copyright (C) 2017 by Christoph Thelen                                #
#   doc_bacardi@users.sourceforge.net                                     #
#                                                                         #
#   This program is free software; you can redistribute it and/or modify  #
#   it under the terms of the GNU General Public License as published by  #
#   the Free Software Foundation; either version 2 of the License, or     #
#   (at your option) any later version.                                   #
#                                                                         #
#   This program is distributed in the hope that it will be useful,       #
#   but WITHOUT ANY WARRANTY; without even the implied warranty of        #
#   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the         #
#   GNU General Public License for more details.                          #
#                                                                         #
#   You should have received a copy of the GNU General Public License     #
#   along with this program; if not, write to the                         #
#   Free Software Foundation, Inc.,                                       #
#   59 Temple Place - Suite 330, Boston, MA  02111-1307, USA.             #
#-------------------------------------------------------------------------#


#----------------------------------------------------------------------------
#
# Set up the Muhkuh Build System.
#

SConscript('mbs/SConscript')
Import('atEnv')

import os.path
import tarfile


#----------------------------------------------------------------------------
#
# Depack the source archive.
#
tSrcArchive = tarfile.open('date-version_2.1.2.tar.gz', 'r')
tSrcArchive.extractall('targets/depack')
tSrcArchive.close()
strDepackPath = 'targets/depack/date-version_2.1.2/'

#----------------------------------------------------------------------------
#
# Build the artifacts.
#

strGroup = 'com.github.tieske'
strModule = 'date'

# Split the group by dots.
aGroup = strGroup.split('.')
# Build the path for all artifacts.
strModulePath = 'targets/jonchki/repository/%s/%s/%s' % ('/'.join(aGroup), strModule, PROJECT_VERSION)


# Set the name of the LUA5.1 artifact.
strArtifact51 = 'lua5.1-date'

tArcList51 = atEnv.DEFAULT.ArchiveList('zip')

tArcList51.AddFiles('',
                    'installer/lua5.1/install.lua')

tArcList51.AddFiles('lua/',
                    os.path.join(strDepackPath, 'date.lua'))

tArtifact51 = atEnv.DEFAULT.Archive(os.path.join(strModulePath, '%s-%s.zip' % (strArtifact51, PROJECT_VERSION)), None, ARCHIVE_CONTENTS = tArcList51)
tArtifact51Hash = atEnv.DEFAULT.Hash('%s.hash' % tArtifact51[0].get_path(), tArtifact51[0].get_path(), HASH_ALGORITHM='md5,sha1,sha224,sha256,sha384,sha512', HASH_TEMPLATE='${ID_UC}:${HASH}\n')
tConfiguration51 = atEnv.DEFAULT.Version(os.path.join(strModulePath, '%s-%s.xml' % (strArtifact51, PROJECT_VERSION)), 'installer/lua5.1/%s.xml' % strModule)
tConfiguration51Hash = atEnv.DEFAULT.Hash('%s.hash' % tConfiguration51[0].get_path(), tConfiguration51[0].get_path(), HASH_ALGORITHM='md5,sha1,sha224,sha256,sha384,sha512', HASH_TEMPLATE='${ID_UC}:${HASH}\n')
tArtifact51Pom = atEnv.DEFAULT.ArtifactVersion(os.path.join(strModulePath, '%s-%s.pom' % (strArtifact51, PROJECT_VERSION)), 'installer/lua5.1/pom.xml')


# Set the name of the LUA5.2 artifact.
strArtifact52 = 'lua5.2-date'

tArcList52 = atEnv.DEFAULT.ArchiveList('zip')

tArcList52.AddFiles('',
                    'installer/lua5.2/install.lua')

tArcList52.AddFiles('lua/',
                    os.path.join(strDepackPath, 'date.lua'))

tArtifact52 = atEnv.DEFAULT.Archive(os.path.join(strModulePath, '%s-%s.zip' % (strArtifact52, PROJECT_VERSION)), None, ARCHIVE_CONTENTS = tArcList52)
tArtifact52Hash = atEnv.DEFAULT.Hash('%s.hash' % tArtifact52[0].get_path(), tArtifact52[0].get_path(), HASH_ALGORITHM='md5,sha1,sha224,sha256,sha384,sha512', HASH_TEMPLATE='${ID_UC}:${HASH}\n')
tConfiguration52 = atEnv.DEFAULT.Version(os.path.join(strModulePath, '%s-%s.xml' % (strArtifact52, PROJECT_VERSION)), 'installer/lua5.2/%s.xml' % strModule)
tConfiguration52Hash = atEnv.DEFAULT.Hash('%s.hash' % tConfiguration52[0].get_path(), tConfiguration52[0].get_path(), HASH_ALGORITHM='md5,sha1,sha224,sha256,sha384,sha512', HASH_TEMPLATE='${ID_UC}:${HASH}\n')
tArtifact52Pom = atEnv.DEFAULT.ArtifactVersion(os.path.join(strModulePath, '%s-%s.pom' % (strArtifact52, PROJECT_VERSION)), 'installer/lua5.2/pom.xml')


# Set the name of the LUA5.3 artifact.
strArtifact53 = 'lua5.3-date'

tArcList53 = atEnv.DEFAULT.ArchiveList('zip')

tArcList53.AddFiles('',
                    'installer/lua5.3/install.lua')

tArcList53.AddFiles('lua/',
                    os.path.join(strDepackPath, 'date.lua'))

tArtifact53 = atEnv.DEFAULT.Archive(os.path.join(strModulePath, '%s-%s.zip' % (strArtifact53, PROJECT_VERSION)), None, ARCHIVE_CONTENTS = tArcList53)
tArtifact53Hash = atEnv.DEFAULT.Hash('%s.hash' % tArtifact53[0].get_path(), tArtifact53[0].get_path(), HASH_ALGORITHM='md5,sha1,sha224,sha256,sha384,sha512', HASH_TEMPLATE='${ID_UC}:${HASH}\n')
tConfiguration53 = atEnv.DEFAULT.Version(os.path.join(strModulePath, '%s-%s.xml' % (strArtifact53, PROJECT_VERSION)), 'installer/lua5.3/%s.xml' % strModule)
tConfiguration53Hash = atEnv.DEFAULT.Hash('%s.hash' % tConfiguration53[0].get_path(), tConfiguration53[0].get_path(), HASH_ALGORITHM='md5,sha1,sha224,sha256,sha384,sha512', HASH_TEMPLATE='${ID_UC}:${HASH}\n')
tArtifact53Pom = atEnv.DEFAULT.ArtifactVersion(os.path.join(strModulePath, '%s-%s.pom' % (strArtifact53, PROJECT_VERSION)), 'installer/lua5.3/pom.xml')

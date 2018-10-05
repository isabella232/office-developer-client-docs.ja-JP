---
title: ������ Exchange �A�J�E���g��g�p���܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4e1804bf-4c50-4942-a7ab-9a8caf1be7e5
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 3c0392cd6a885900c1a305cd1cd816a5925745a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398592"
---
# <a name="using-multiple-exchange-accounts"></a>������ Exchange �A�J�E���g��g�p���܂��B

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Microsoft Outlook 2010 および Microsoft Outlook 2013 は、複数の exchange 電子メール アカウントとの統合をサポートします。 Outlook 2010 または Outlook 2013 では、ユーザーが同じプロファイルに 2 つの exchange アカウントを追加を活用し、ながら発行済みのグローバル アドレス一覧 (GAL)、Exchange の出力を Office の構成では、フォルダーの共有など、Exchange の豊富な機能です。
  
Microsoft Office Outlook 2007 用の MAPI プロファイル セクションを理解およびそれ以前は、固定の Exchange のグローバル プロファイル セクションの**pbGlobalProfileSectionGuid**で、電子メール ユーザー名とサーバー名など、Exchange の設定が格納されていることを知る。 Exchange のグローバル プロファイルの詳細については、[グローバル プロファイル セクションを開く方法](https://support.microsoft.com/kb/188482)を参照してください。 Outlook 2010、Outlook 2013 では、各 Exchange アカウントには、 **pbGlobalProfileSectionGuid**を廃止する設定を格納する独自のプロファイル セクションが必要があります。 
  
�v���t�@�C��] �ŁA Outlook 2010��Outlook 2013 Exchange �̐ݒ肪�܂��ۑ�����Ă��邪�A�v���t�@�C�����Ƃ̐ݒ��܂ރZ�N�V�����̃v���t�@�C���̈�ӂ̎��ʎq�����蓖�Ă��Ă��铮�I�ɕύX���܂��B�v���t�@�C���� Exchange �̐ݒ�̏ꏊ�́A[ [PidTagExchangeProfileSectionId ���K���̃v���p�e�B](pidtagexchangeprofilesectionid-canonical-property.md)] �́AExchange �A�J�E���g�̃��b�Z�[�W �T�[�r�X �v���t�@�C��] �Z�N�V�����ɋL�ڂ���Ă���ɕۑ�����܂��B���̃v���p�e�B�́A������Ƃ̏ꍇ�́A���̃��b�Z�[�W �T�[�r�X�̃v���o�C�_�[���Ƃ� [�v���t�@�C��] �Z�N�V�����ɂ�L�ڂ���Ă��܂��B��ӂ̎��ʎq�́A�T�[�o�[�ɕۑ�����Ă��Ȃ��ƁA�v���t�@�C���ňقȂ邪���܂��B
  
Outlook 2010Outlook 2013 **PidTagExchangeProfileSectionId**��ӂ̎��ʎq�Ƃ��Ă�g���� Exchange �A�J�E���g��w�肵�܂��B���̕��@�Ŏg�p����ꍇ�A��ӂ̎��ʎq�� **emsmdbUID**�ƌĂ΂�܂��BMAPI �����Outlook����ɂ���āA **emsmdbUID**������Ɏg�p���� Exchange �A�J�E���g��w�肷��K�v����܂��B 
  
������ Exchange �A�J�E���g��T�|�[�g���邽�߂ɁA�R�[�h�̈ꕔ�̐V�����֐��̌Ăяo����g�p���Ă��������B**IMailUser: IMAPIProp**�ƁA���̊֐��� 1 ��[IDistList: IMAPIContainer](iaddrbook-openentry.md)�� [entryID](iaddrbook-compareentryids.md)��[IAddrBook::OpenEntry](imailuserimapiprop.md)�܂���[IAddrBook::CompareEntryIDs](idistlistimapicontainer.md)��g�p���Ă��邷�ׂĂ̌Ăяo����u�������܂��B 
  
- [HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
    
- [HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
    
- [HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
    
- [HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
    
- [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
    
- [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
    
- [HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
    
- [HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
    
- [HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
    
## <a name="legacy-support"></a>�]���̃T�|�[�g

���̐V���� **emsmdbUID**�Z�N�V������쐬����O�ɋL�q MAPI �N���C�A���g�͈��������T�|�[�g����܂��B�����̃N���C�A���g�͈��������O���[�o���O�̃Z�N�V���� **pbGlobalProfileSectionGuid**��擾���܂��B���̃v���t�@�C��] �Z�N�V�����̃N�G���́A�]���̏Ɖ��������� 1 �̎w�肳�ꂽ Exchange �A�J�E���g�Ƀ��_�C���N�g����܂��B�]���̌Ăяo�����������A�J�E���g�́A���b�Z�[�W �T�[�r�X �e�[�u������āAPR_EMSMDB_LEGACY �̗��ǉ����Ċm�F�ł��܂��B1 �̃��b�Z�[�W �T�[�r�X�݂͂̂ɐݒ肳��A���� **PidTagExchangeProfileSectionId** true �̏ꍇ�A����́A�]���� **emsmdbUID**�ƌĂ΂�܂��B
  
> [!NOTE]
> [!����] ����̃X�g�A�Ɗ���̃A�J�E���g�Ȃǂ� MAPI �ݒ�́A�A�J�E���g���]���̌Ăяo����������邽�߂̉e����^����Ȃ��B�]���̌Ăяo�����������A�J�E���g��\�����邱�Ƃ͂ł��܂���B 
  
�]���̃A�J�E���g�� **emsmdbUID**��Outlook�O���[�o�� �v���t�@�C��] �Z�N�V�����ɃR�s�[����܂��B���̃v���p�e�B�����݂��Ȃ��ꍇ�A���b�Z�[�W�̃T�[�r�X�̃e�[�u���̃N�G������s����ƁA�ǂ̂悤�ȃA�J�E���g���A�]���̃n���h���[�ł��邱�Ƃ�m�F���A Outlook�O���[�o�� �v���t�@�C��] �Z�N�V�����Œl��ݒ肵�܂��B 
  
�I�t�ɂ���ƁAExchange �O���[�o�� �v���t�@�C�� �Z�N�V��������O���[�o�� �v���t�@�C��] �Z�N�V�������قȂ�Outlook����Outlook 2010�����Outlook 2013�� Exchange �̃O���[�o�� �v���t�@�C��] �Z�N�V�����͂���܂���O���[�o���{���ɕ����� Exchange �A�J�E���g�����邱�Ƃ��ł��܂��BOutlook�O���[�o�� �v���t�@�C��] �Z�N�V�����ɂ́A Outlook�A�ŋߎg�p�����t�H���_�[�̏�ԁA�܂��̓O���[�o���ڑ��̏�ԂȂǂ̃v���p�e�B���܂܂�Ă��܂��B
  
## <a name="address-book-account-contexts"></a>�A�h���X���̃A�J�E���g�̃R���e�L�X�g

������ Exchange �A�J�E���g�Ő������A�h���X��������ɂ́A�A�h���X���ɒʘb�������� Exchange �A�J�E���g������ł���悤�ɁA�A�J�E���g�̃R���e�L�X�g���V�����@�\��g�p���܂��B
  
Api ���ꂽ�@�\������S�ɕ����� Exchange �ł͂Ȃ����߂ɁA�������O�̃A�h���X���� Api �͔p�~����܂����B���̃A�J�E���g�̃R���e�L�X�g�́A�ʏ�A **emsmdbUID**�ł��B
  
������ Exchange �A�J�E���g�ɂ́A **emsmdbUID**�ł́A�ɉ����āA **emsabpUID**�������܂��B
  
1. **emsmdbUID**�l�́A�A�J�E���g�̃R���e�L�X�g������܂��B 
    
2. **emsabpUID**�l�́AExchange �A�h���X��������܂��B 
    
**emsabpUID**�l�͒ʏ�A��M�҂�������Ƃ��Ɏg�p����܂��B[IAddrBook::ResolveName](iaddrbook-resolvename.md)��g�p���Ď�M�҂�������ɂ́AExchange ��M�҂̍s�ɂ́A **emsabpUID**�l��܂ށA **PR_AB_PROVIDERS** (0x3D010102) �v���p�e�B���܂܂�Ă��܂��B���� **emsabpUID**�l�́A����̎�M�҂� Exchange �A�h���X����w�肵�܂��B 
  
����� **emsmdbUID** **emsabpUID**�l��w�肷��ꍇ�́A **emsmdbUID**�̃v���t�@�C���̃Z�N�V������J���A **PR_EMSABP_USER_UID** (0x0x3D1A0102) �̃v���p�e�B��擾���܂��B 
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)�A�Ăяo���ꍇ�������X�g��� Exchange ��M�҂��A��M�҂���������A�h���X���ɑΉ����� **emsabpUID**�� **PR_AB_PROVIDERS**�v���p�e�B���܂܂�Ă��邱�Ƃ�m�F���܂��B�ǉ��̑����K�v�Ƃ��Ȃ�[IAddrBook::ResolveName](iaddrbook-preparerecips.md)����擾�����s��[IAddrBook::PrepareRecips](iaddrbook-resolvename.md)��Ăяo�����Ƃ��������̃R�[�h�ɓd�b�������[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) **PR_ENTRYID**�v���p�e�B�݂̂��܂܂�Ă���s�B���̍s�Ɠ����悤�ȏ󋵂� **PR_AB_PROVIDERS**�v���p�e�B�ɓK�؂� **emsabpUID**�� **PR_ENTRYID**�� **PR_AB_PROVIDERS**�̗�����܂߂�K�v������܂��B
  
������ Exchange �A�J�E���g�������邽�߂̃v���Z�X�̊ȒP�Ȑ���́A���̂Ƃ���ł��B
  
- �T�[�r�X�̈�ӂ̎��ʎq��w�肷��ɂ́A�R�[�h�́A **PR_SERVICE_UID**�v���p�e�B�������̂ƈ�v���郁�b�Z�[�W �X�g�A�̃e�[�u���Ō������܂��B��������́A������ **PR_MDB_PROVIDER**��w��ł��܂��B���̍s�ɂ́A�K�؂ȃX�g�A���܂܂�Ă��܂��B
    
- �R�[�h�� **emsmdbUID**��w�肷��ƁA **emsmdbUID**�Ɉ�v���� **PidTagExchangeProfileSectionId**����J����s�̃��b�Z�[�W �T�[�r�X �e�[�u�����\������܂��B
    
## <a name="see-also"></a>�֘A����



[HrCompareABEntryIDsWithExchangeContext](hrcompareabentryidswithexchangecontext.md)
  
[HrDoABDetailsWithExchangeContext](hrdoabdetailswithexchangecontext.md)
  
[HrDoABDetailsWithProviderUID](hrdoabdetailswithprovideruid.md)
  
[HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)
  
[HrOpenABEntryUsingDefaultContext](hropenabentryusingdefaultcontext.md)
  
[HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md)
  
[HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md)
  
[HrOpenABEntryWithProviderUIDSupport](hropenabentrywithprovideruidsupport.md)
  
[HrOpenABEntryWithResolvedRow](hropenabentrywithresolvedrow.md)
  
[HrOpenABEntryWithSupport](hropenabentrywithsupport.md)
  
[PidTagExchangeProfileSectionId ���K���̃v���p�e�B](pidtagexchangeprofilesectionid-canonical-property.md)


[[�O���[�o�� �v���t�@�C��] �Z�N�V������J�����@](https://support.microsoft.com/kb/188482)


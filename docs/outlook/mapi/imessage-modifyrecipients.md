---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
ms.openlocfilehash: f8cca47a25157379e6005ca5b0f2dd7cbe934015
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551283"
---
# <a name="imessagemodifyrecipients"></a>IMessage::ModifyRecipients

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
�ǉ��A�폜�A�܂��̓��b�Z�[�W�̎�M�҂�ύX���܂��B
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]��M�҂̕ύX�𐧌䂷��t���O�̃r�b�g���܂��B _ulFlags_�p�����[�^�[�̃[����o�߂���ƁA **ModifyRecipients**�� _lpMods_�p�����[�^�[�Ŏw�肳�ꂽ����̃��X�g�Ŋ����̂��ׂĂ̎�M�҂�u�������܂��B _ulFlags_�ɂ́A���̃t���O��ݒ�ł��܂��B
    
MODRECIP_ADD 
  
> _lpMods_�p�����[�^�[��w����M�҂́A����̃��X�g�ɒǉ�����K�v������܂��B 
    
MODRECIP_MODIFY 
  
> _lpMods_�p�����[�^�[��w����M�҂́A�����̎�M�҂ɒu�������Ă��������B���ׂĂ̊����̃v���p�e�B�́A�Ή�����[ADRENTRY](adrentry.md)�\����ɒu���������܂��B 
    
MODRECIP_REMOVE 
  
> _lpMods_ パラメーター内の各受信者エントリのプロパティ値配列に含まれる **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) プロパティをインデックスとして使用して、既存の受信者を受信者リストから削除する必要があります。 
    
 _lpMods_
  
> [����]�|�C���^�[��ǉ��A�폜�A�܂��̓��b�Z�[�W��ɕύX���ꂽ����̃��X�g��܂�[ADRLIST](adrlist.md)�\���ɂ��܂��B 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ���惊�X�g������ɕύX����܂����B
    
## <a name="remarks"></a>注釈

**IMessage::ModifyRecipients**���\�b�h�́A���b�Z�[�W�̎�M�҃��X�g��ύX���܂��B���̃��X�g����A��M�҂̃e�[�u�����g�ݍ��܂�Ă���A [ADRLIST](adrlist.md)�\����ɕێ��͂ł��܂��B 
  
**ADRLIST**�\���̊e��M�҂� 1 ��[ADRENTRY](adrentry.md)�\�����܂܂�Ă��邵�A�e **ADRENTRY**�\���ɂ́A��M�҂̃v���p�e�B��L�q����v���p�e�B�̒l�̔z�񂪊܂܂�Ă��܂��B 
  
**ADRLIST 構造の受信者** は、解決または未解決にできます。 違いは、含まれるプロパティの数と種類です。 未解決の受信者には **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと PR_RECIPIENT_TYPE ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティだけが含まれるのに対し、解決された受信者には **これらの 2** つのプロパティと PR_ADDRTYPE ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) と **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)が含まれる。  **[PR_EMAIL_ADDRESS** ] ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) を使用できる場合は、このアドレスも含めできます。
  
���b�Z�[�W�����M�����܂łɂ́A���̎�M�҈ꗗ�ŉ����M�҂݂̂ɕK�v������܂��B��M�҂ɂ́A�z�M�s�\���|�[�g��쐬���A���̃��b�Z�[�W�̑��M�҂ɑ��M���ꂽ���������܂��B�N���C�A���g�̊ϓ[���疼�O����v���Z�X�̏ڍׂɂ��ẮA[���O��������](resolving-a-recipient-name.md)��Q�Ƃ��Ă��������B�A�h���X���̃v���o�C�](resolving-a-recipient-name.md)�[�̊ϓ_����̏ڍׂɂ��ẮA[���O������������](implementing-name-resolution.md)��Q�Ƃ��Ă��������B
  
�ɉ����ĉ������і�����̎�M�҂��M�҂� NULL ���Ƃ��ł��܂��B��M�҂� **ADRENTRY**�\���� **cValues**�����o�[�� 0 �ɐݒ肵�A **rgPropVals**�����o�[�� NULL �ɐݒ肵�܂��B 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

You can create a recipient list by calling [IAddrBook::Address](imapisupport-address.md) to display the common dialog box and prompt the user to select entries. The address list pointed to by the  _lppAdrList_ parameter to **Address** can be passed to **ModifyRecipients** as the  _lpMods_ parameter. 
  
[ADRLIST](adrlist.md)�\����Ŏ�M�҂̃v���p�e�B��w�肷��ꍇ�́A���ׂĂ̒ǉ��܂��͕ύX���ꂽ��̂����łȂ��A��M�҂̃v���p�e�B��w�肵�܂��B��M�҂��ύX���ꂽ�Ƃ� **ADRLIST**�\���Ɋ܂܂�Ă��Ȃ��C�ӂ̃v���p�e�B���폜����܂��B���݂̈�A�̃v���p�e�B�̂��ׂẴ��b�Z�[�W�̎�M�҂�擾����ɂ͂���ɂ́A [GetRecipientTable](imessage-getrecipienttable.md)����ׂĂ̍s��擾���܂��B **SRowSet**�ɂ́A **ADRLIST**�\����Ɠ����ł��邽�ߓ����Ӗ��Ŏg�p�ł��܂��B
  
 **ModifyRecipients**�ɂ́A  _ulFlags_�p�����[�^�[�Ȃ��̃t���O�̐ݒ肳��Ă���ꍇ�A  _lpMods_���w������܂ނ��ׂĂ̌��݂̎�M�҃��X�g�̃G���g�����u���������܂��B 

MODRECIP_MODIFY �t���O��ݒ肷��Ƃ��� **ModifyRecipients** [lpMods](adrlist.md)�ɓn�����_ADRLIST_�\���Ɋ֘A�t�����Ă���s�S�̂̎�M�Ҋe�s�ɒu�������܂��B���ׂĂ̎�M�҂��Ӑ}�����ɍ폜����Ȃ��悤�ɕύX����Ă��邩�ǂ����Ɋ֌W�Ȃ��A�v���p�e�B��w�肷��悤�ɒ��ӂ��܂��B
  
�ȉ��́A **ADRLIST**�\���Ŏ�M�҂̃v���p�e�B��ݒ肷�邽�߂̂������̃��[���ł��B 
  
- �v���p�e�B�̌^�Ƃ��� PT_NULL ��g��Ȃ��ł��������B **ModifyRecipients** �ł́A���̒l�����������ꍇ�A�G���[���Ԃ���܂��B 
    
- �v���p�e�B�̌^�Ƃ��� PT_ERROR ��g��Ȃ��ł��������B **ModifyRecipients** �ł́A���̒l�͖������܂��B 
    
- **ulFlags**�� MODRECIP_REMOVE �܂��� MODRECIP_MODIFY �̂����ꂩ�̃t���O��ݒ肷��ƁA���ׂĂ̎�M�҂ɑ΂��āA _PR_ROWID_�v���p�e�B���܂܂�܂��B 
    
- **ulFlags**�܂��� _ulFlags_�Ƀ[����ʉ߂���Ƃ��ɁAMODRECIP_ADD �t���O��ݒ肷��Ƃ��ɁA��M�҂̂����ꂩ�� _PR_ROWID_�v���p�e�B��܂߂Ȃ��ł��������B
    
��M�҂� 1 �� **PR_ADDRTYPE**�v���p�e�B�܂��� **PR_EMAIL_ADDRESS**�v���p�e�B��ǉ�����A�܂��͗����̃v���p�e�B�� **PR_ENTRYID**�Ŏ������悤�ɁA��M�҂̃A�h���X�A�Z���̎�ނƈ�v���Ȃ��A���ʂ͒�`����Ă��܂���B�܂�A�T�[�r�X �v���o�C�_�[�ɂ���ẮA���� 3 �̉\��������܂��B
  
- ���b�Z�[�W�́A **PR_ADDRTYPE**�� **PR_EMAIL_ADDRESS**�v���p�e�B�Ő������Ă���A�h���X�ɔz�M����܂��B 
    
- **PR_ENTRYID**�Ŏ����ꂽ��M�҂Ƀ��b�Z�[�W���z�M����܂��B
    
- ���b�Z�[�W�́A�Z���̂����܂����������Ŕz�M�s�\�錾����܂��B
    
���惊�X�g�̃��������蓖��[ADRLIST �� SRowSet �\���̃�������Ǘ�����](managing-memory-for-adrlist-and-srowset-structures.md)�Ő�����Ă��銄�蓖�ă��[����g�p���܂��B **ADRLIST**�\����̃T�u�\���̂����ꂩ�� **ModifyRecipients**�������܂���B **ADRLIST**�\���Ɗe [SPropValue](spropvalue.md)�\���̂́A���ꂼ��ʂɉ�����邱�Ƃ��ł��܂����A [MAPIAllocateBuffer](mapiallocatebuffer.md)�֐���g�p���ČʂɊ��蓖�Ă���K�v������܂��B���@�ł́A�C�ӂ� **SPropValue**�\���̒ǉ��̗̈��K�v�Ƃ���ꍇ�A���Ƃ��ł��܂� **SPropValue**�\����Œu��������V����[MAPIFreeBuffer](mapifreebuffer.md)��g�p���Č�ŉ���ł��܂��B **MAPIFreeBuffer**��g�p���Ă�A���� **SPropValue**�\����������K�v������܂��B
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI �ł́A **IMessage::ModifyRecipients**���\�b�h��g�p���āA���b�Z�[�W�ɁA�V������M�҂�ǉ����܂��B  <br/> |
   
## <a name="see-also"></a>関連項目



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)


---
title: MAPI ��M��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 88a4360d-6ab8-466e-8ebd-af80227ee00a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6af54b773b875531437a275f14c961a06ef799ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569520"
---
# <a name="mapi-recipients"></a>MAPI ��M��

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
���ׂẴ��b�Z�[�W�𑗐M����̂ɂ́A1 �܂��͕����̈���A�܂��͈�A�̃��b�Z�[�W�̔z�M���\���v���p�e�B�����܂��B��M�҂����b�Z�[�W�̃R���e�L�X�g�ł̂ݎg�p���邽�� MAPI �̌ʂ̃I�u�W�F�N�g�̑���Ƀ��b�Z�[�W�̃I�u�W�F�N�g�ƌ��Ȃ���܂��B�N���C�A���g�ƃv���o�C�_�[ **IMessage** �C���^�[�t�F�C�X��g�p���Ď�M�҂�g�p���܂��B�ڍׂɂ��ẮA [IMessage: IMAPIProp](imessageimapiprop.md)��Q�Ƃ��Ă��������B
  
�N���C�A���g�ł́A���̎�M�҂̃e�[�u������A���b�Z�[�W�̎�M�҂��A�N�Z�X���܂��B���ׂẴ��b�Z�[�W�ɂ́A��M�҂��M�҂̂��ꂼ��ɂ��Ă̊T�v����܂ރe�[�u��������܂��B�e�[�u���Ɋ܂܂�Ă����́A���b�Z�[�W�̏�Ԃɂ���ĈقȂ�܂��B���b�Z�[�W�́A[�\�����A���̎�M�҂́A�\��� 3 ��݂̂�����܂��B
  
- 表示名、または**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- 受信者の種類、または**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- 行識別子、または**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
メッセージには、名前解決の処理が行われましたが、各受信者もがエントリの識別子、または**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) の列です。 メッセージが送信されると、受信者テーブルの行が 2 つ以上の列を追加します。
  
- アドレスの種類、または**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- トランスポートの役割または**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
クライアントは、その**IMessage::GetRecipientTable**メソッドまたは**IMAPIProp::OpenProperty**メソッドを呼び出すことによって、メッセージの受信者テーブルを取得できます。 詳細については、 [IMessage::GetRecipientTable](imessage-getrecipienttable.md)および[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。 メッセージ ストア プロバイダーは、これらの方法の両方をサポートする必要があります。 **OpenProperty**のアプローチでは、クライアントがインターフェイス識別子とプロパティ タグと**PR_MESSAGE_RECIPIENTS**として IID_IMAPITable を指定することが必要です。 **PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) は、メッセージの受信者テーブルを表すテーブル オブジェクトのプロパティです。 メッセージ ストア プロバイダーは、メッセージごとに**PR_MESSAGE_RECIPIENTS**を設定し、 **IMAPIProp::GetPropList**メソッドから返されるプロパティ タグの配列に追加する必要があります。 詳細については、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)を参照してください。
  
��M�҂̃e�[�u���𑀍삷����@�̏ڍׂɂ��ẮA [��M�҂̃e�[�u��](recipient-tables.md)��Q�Ƃ��Ă��������B
  
��M�҂̃e�[�u���ɃA�N�Z�X���邽�߂Ɏg�p����Ă���A�ɉ����� **PR_MESSAGE_RECIPIENTS**��g�p�ł��܂��B 
  
- **IMAPIProp::CopyTo** �܂��͏��O����A�܂��̓R�s�[����Ƃ��ɁA��M�҂�܂߂�ɂ́A **IMAPIProp::CopyProps** ���܂��B���̑��̏���Q�Ƃ��Ă��������A [IMAPIProp::CopyTo](imapiprop-copyto.md)�����[IMAPIProp::CopyProps](imapiprop-copyprops.md)���܂��B
    
- �q�̐�������M�҂ɓK�p���邩��������ʐ������܂��B
    
MAPI アドレス帳からエントリをコピーするか、新しいエントリを作成することによって、クライアントはメッセージに受信者を追加できます。 一時アドレスと呼ばれる、これらの新しいエントリでは、一時的に存在することがまたは変更可能なコンテナー内で永続的に保存されます。 受信者をアドレス帳から取得されますがある、エントリの id がアドレス帳プロバイダーに関連付けられている、1 回限りの受信者は MAPI によってフォーマットされているエントリの識別子をあります。 トランスポート プロバイダーとさまざまな種類のアドレスを持つクライアント関連の 1 回限りのエントリの識別子です。 
  
�g�����X�|�[�g �v���o�C�_�[�ʘb **IMAPISupport::CreateOneOff** ���M�̃A�h���X�� 1 �����̃G���g�����ʎq��쐬���郁�b�Z�[�W�̏ꍇ�B 
  
- �A�h���X�������Ă���Q�[�g�E�F�C���܂��B
    
- ���݂̃v���t�@�C���ŃA�h���X���v���o�C�_�[�ɂ���ẮA�A�h���X��������邱�Ƃ͂ł��܂���B
    
�ڍׂɂ��ẮA [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)��Q�Ƃ��Ă��������B
  
�N���C�A���g����M�Z���ꎞ�G���g�����ʎq��쐬����̂ɂ́A **IAddrBook::CreateOneOff** ��Ăяo�����b�Z�[�W�̏ꍇ�B 
  
- �A�h���X�́A1 �����̃A�h���X�Ƃ��Đݒ肳��܂��B
    
- �A�h���X�́A�C���^�[�l�b�g �A�h���X�Ƃ��Đݒ肳��܂��B
    
�ڍׂɂ��ẮA [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)��Q�Ƃ��Ă��������B
  
�ڍׂɂ��ẮA1 �����̃G���g�����ʎq�ƃA�h���X�A [1 �����̃G���g�����ʎq](one-off-entry-identifiers.md)��[1 �����̃A�h���X](one-off-addresses.md)��Q�Ƃ��Ă��������B
  
��M�҂̃v���p�e�B�́A�A�h���X���̃v���p�e�B�ƈ���̈���ɌŗL�̃v���p�e�B�̑g�ݍ��킹�ł��B���ׂĂ̎�M�҂ɂ́A�A�h���X���v���o�C�_�[�ɂ���Ċ��蓖�Ă��Ă���A�x�[�X �A�h���X �v���p�e�B������܂��B�G���g���́A���M���b�Z�[�W�̎�M�҂Ƃ��Ďg�p�����̃x�[�X �A�h���X �v���p�e�B�́A���ׂẴ��b�Z�[�W�̎�M�҂̃v���p�e�B��ێ����� **ADRLIST** �\���ɃR�s�[����܂��B 
  
��M�җp�ɐݒ肳��Ă��� 2 �̃v���p�e�B�́A **PR_RECIPIENT_TYPE** **PR_RESPONSIBILITY**�ł��B **PR_RECIPIENT_TYPE**�́A��M�҂��v���C�}���Acarbon copy �̗��A�u���C���h �J�[�{�� �R�s�[�A�܂��͍đ��M�����M�҂��ǂ���������܂��B�ŏ��� 3 �̎�ނ́A�ŏ��ɑ��M����郁�b�Z�[�W�̎�M�҂Ɋ��蓖�Ă��܂��B 
  
��M�҂Ƀ��b�Z�[�W���\������Ȃ��ꍇ�́A�����đ��M���悤�Ƃ��܂������A��M�҂��R�s�[����܂�����̎�ސݒ肪 MAPI_P1 ��đ��M���鈶���w�肵�܂��B�ꕔ�̎�M�҂ɂ́A���b�Z�[�W���\�������A�����̏ꍇ�A���� **PR_RECIPIENT_TYPE**�v���p�e�B�́A���b�Z�[�W��đ������Ƃ� MAPI_SUBMITTED �t���O�̓�e�ƃ}�[�N����܂��B�N���C�A���g�̓v���C�}���̎�M�҂�������邽�߂ɕK�v�Ȃ܂��́A **PR_RECIPIENT_TYPE**�����M�҂� MAPI_TO �ɐݒ肵�܂��B���̑��̂��ׂĂ̎�ނ̓I�v�V�����ł��B 
  
 **れない**は、トランスポート プロバイダーに受信者への送信を処理するように動作しているかどうかを示すために設定されています。 送信メッセージが送信されると、すべての受信者**れない**を FALSE に設定します。 トランスポート プロバイダーは、1 つまたは複数の受信者に送信するための責任を主張とその**れない**プロパティが TRUE に設定します。 
  


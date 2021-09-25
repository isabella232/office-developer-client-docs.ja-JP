---
title: MAPI �̓Y�t�t�@�C��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c4e8543455547d09f0ee67b66a9a0a504905b95c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567278"
---
# <a name="mapi-attachments"></a>MAPI �̓Y�t�t�@�C��

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のメッセージ ストア プロバイダーでは、クライアントが追加された情報をファイル、OLE オブジェクト、メッセージ、またはバイナリ データの形式でメッセージに関連付けできます。 この追加された情報は、メッセージの添付ファイルと呼ばれる。 添付ファイルはメッセージを通じてのみ作成、管理、およびアクセスされるので、メッセージ サブオブジェクトと見なされます。 添付ファイルは、アクセス用のエントリ識別子を持つのではなく、添付ファイル番号と呼ばれる連続した番号を持つ。 この番号は、メッセージ内の添付ファイルを一意に識別しますが、必ずしもメッセージ ストア内ではありません。 2 つの異なるメッセージには、同じ添付ファイル番号を持つ異なる添付ファイルを含めできます。 添付ファイル番号は、メッセージが開いている限り有効で、PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティに格納されます。
  
���ׂẴ��b�Z�[�W�̓Y�t�t�@�C���ɂ��Ă̊T�v���ɃA�N�Z�X����ɂ́A�N���C�A���g�́A���̓Y�t�t�@�C���̃e�[�u����擾���܂��B�Y�t�t�@�C���̃e�[�u���ɂ́A�Y�t�t�@�C����Y�t�t�@�C���̐��A���R�[�h �L�[�Ȃǂɒ��ڃA�N�Z�X �N���C�A���g��g�p���Ă����񂪊܂܂�܂��B�N���C�A���g�ł̓Y�t�t�@�C���̃e�[�u����擾�ł��܂��B
  
- **IMessage::GetAttachmentTable** �𔭐M���܂��B�ڍׂɂ��ẮA [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)��Q�Ƃ��Ă��������B
    
- **IMAPIProp::OpenProperty** �𔭐M���܂��B�ڍׂɂ��ẮA [IMAPIProp::OpenProperty](imapiprop-openproperty.md)��Q�Ƃ��Ă��������B
    
Message store providers are expected to support both of these approaches. **OpenProperty** アプローチでは、呼び出し元が IID_IMAPITable をインターフェイス識別子として **、PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) をプロパティ タグとして指定する必要があります。 **PR_MESSAGE_ATTACHMENTS** は、メッセージの添付ファイル テーブルを表すテーブル オブジェクト プロパティです。 メッセージ ストア プロバイダーは、各メッセージPR_MESSAGE_ATTACHMENTSを設定し **、IMAPIProp::GetPropList** メソッドから返されるプロパティ タグの配列に含める必要があります。 For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
 **PR_MESSAGE_ATTACHMENTS**��g�p�ł��܂��B 
  
- **IMAPIProp::OpenProperty** ��A�Y�t�t�@�C���܂��͎�M�҂̃e�[�u���ɃA�N�Z�X���܂��B 
    
- **IMAPIProp::CopyTo** �܂��͏��O����A�܂��̓R�s�[����Ƃ��ɁA�Y�t�t�@�C����܂߂�ɂ́A **IMAPIProp::CopyProps** ���܂��B�ڍׂɂ��ẮA [IMAPIProp::CopyTo](imapiprop-copyto.md)��[IMAPIProp::CopyProps](imapiprop-copyprops.md)��Q�Ƃ��Ă��������B
    
- �q�̐����� [�Y�t�t�@�C���ɓK�p���邩��������ʐ������܂��B
    
�ڍׂɂ��ẮA [�Y�t�t�@�C���̃e�[�u��](attachment-tables.md)��Q�Ƃ��Ă��������B
  


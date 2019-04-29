---
title: MAPI �̓Y�t�t�@�C��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 90fbec8b61499f383228823d69b041a21199a22e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417834"
---
# <a name="mapi-attachments"></a>MAPI �̓Y�t�t�@�C��

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のメッセージストアプロバイダーを使用すると、クライアントは、追加された情報をファイル、OLE オブジェクト、メッセージ、またはバイナリデータ形式でメッセージに関連付けることができます。 この追加情報は、メッセージの添付ファイルと呼ばれます。 添付ファイルは、メッセージによってのみ作成、管理、およびアクセスされるので、メッセージサブオブジェクトと見なされます。 添付ファイルには、access のエントリ識別子を指定しなくても、添付ファイル番号と呼ばれる連続番号が付けられます。 この番号は、メッセージ内の添付ファイルを一意に識別しますが、メッセージストア内にあるとは限りません。 2つの異なるメッセージは、同じ添付ファイル番号を持つ複数の添付ファイルを持つことができます。 添付ファイルの番号は、メッセージが開かれていて、 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティに格納されている場合に限り有効です。
  
���ׂẴ��b�Z�[�W�̓Y�t�t�@�C���ɂ��Ă̊T�v���ɃA�N�Z�X����ɂ́A�N���C�A���g�́A���̓Y�t�t�@�C���̃e�[�u����擾���܂��B�Y�t�t�@�C���̃e�[�u���ɂ́A�Y�t�t�@�C����Y�t�t�@�C���̐��A���R�[�h �L�[�Ȃǂɒ��ڃA�N�Z�X �N���C�A���g��g�p���Ă����񂪊܂܂�܂��B�N���C�A���g�ł̓Y�t�t�@�C���̃e�[�u����擾�ł��܂��B
  
- **IMessage::GetAttachmentTable** �𔭐M���܂��B�ڍׂɂ��ẮA [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)��Q�Ƃ��Ă��������B
    
- **IMAPIProp::OpenProperty** �𔭐M���܂��B�ڍׂɂ��ẮA [IMAPIProp::OpenProperty](imapiprop-openproperty.md)��Q�Ƃ��Ă��������B
    
Message store providers are expected to support both of these approaches. **openproperty**アプローチでは、呼び出し元が IID_IMAPITable をインターフェイス識別子として指定し、 **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) をプロパティタグとして指定する必要があります。 **PR_MESSAGE_ATTACHMENTS**は、メッセージの添付ファイルテーブルを表す table オブジェクトプロパティです。 メッセージストアプロバイダーは、メッセージごとに**PR_MESSAGE_ATTACHMENTS**を設定し、 **imapiprop:: getproplist**メソッドから返されたプロパティタグの配列に含める必要があります。 For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
 **PR_MESSAGE_ATTACHMENTS**��g�p�ł��܂��B 
  
- **IMAPIProp::OpenProperty** ��A�Y�t�t�@�C���܂��͎�M�҂̃e�[�u���ɃA�N�Z�X���܂��B 
    
- **IMAPIProp::CopyTo** �܂��͏��O����A�܂��̓R�s�[����Ƃ��ɁA�Y�t�t�@�C����܂߂�ɂ́A **IMAPIProp::CopyProps** ���܂��B�ڍׂɂ��ẮA [IMAPIProp::CopyTo](imapiprop-copyto.md)��[IMAPIProp::CopyProps](imapiprop-copyprops.md)��Q�Ƃ��Ă��������B
    
- �q�̐����� [�Y�t�t�@�C���ɓK�p���邩��������ʐ������܂��B
    
�ڍׂɂ��ẮA [�Y�t�t�@�C���̃e�[�u��](attachment-tables.md)��Q�Ƃ��Ă��������B
  


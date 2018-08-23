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
ms.openlocfilehash: fd8075d2fddb7ada6803c869cbbd282c464e75bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585879"
---
# <a name="mapi-attachments"></a>MAPI �̓Y�t�t�@�C��

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
いくつかのメッセージ ストア プロバイダーは、ファイル、OLE オブジェクト、メッセージ、またはバイナリ データの形式で追加情報をメッセージに関連付けるクライアントを有効にします。 この追加情報は、メッセージの添付ファイルと呼ばれます。 添付ファイルが作成、管理し、自分のメッセージのみを使用してアクセス、ためメッセージの下位オブジェクトと見なされます。 エントリ識別子にアクセスするのではなく、添付ファイルの数と、添付ファイルで連続した番号の正常があります。 この番号は、メッセージ内ではなくとも、メッセージ ・ ストア内の添付ファイルを一意に識別します。 2 種類のメッセージは、添付ファイルの数が同じ別の添付ファイルを持つことができます。 添付ファイル番号は、メッセージが開かれていて、 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティに格納されている限りにのみ有効です。
  
���ׂẴ��b�Z�[�W�̓Y�t�t�@�C���ɂ��Ă̊T�v���ɃA�N�Z�X����ɂ́A�N���C�A���g�́A���̓Y�t�t�@�C���̃e�[�u����擾���܂��B�Y�t�t�@�C���̃e�[�u���ɂ́A�Y�t�t�@�C����Y�t�t�@�C���̐��A���R�[�h �L�[�Ȃǂɒ��ڃA�N�Z�X �N���C�A���g��g�p���Ă����񂪊܂܂�܂��B�N���C�A���g�ł̓Y�t�t�@�C���̃e�[�u����擾�ł��܂��B
  
- **IMessage::GetAttachmentTable** �𔭐M���܂��B�ڍׂɂ��ẮA [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)��Q�Ƃ��Ă��������B
    
- **IMAPIProp::OpenProperty** �𔭐M���܂��B�ڍׂɂ��ẮA [IMAPIProp::OpenProperty](imapiprop-openproperty.md)��Q�Ƃ��Ă��������B
    
メッセージ ストア プロバイダーは、これらの方法の両方をサポートする必要があります。 **OpenProperty**のアプローチでは、呼び出し元が、プロパティ タグとして、インターフェイス識別子と**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) として IID_IMAPITable を指定する必要があります。 **PR_MESSAGE_ATTACHMENTS**は、メッセージの添付ファイル テーブルを表すテーブル オブジェクトのプロパティです。 メッセージ ストア プロバイダーは、メッセージごとに**PR_MESSAGE_ATTACHMENTS**を設定し、 **IMAPIProp::GetPropList**メソッドから返されるプロパティ タグの配列に追加する必要があります。 詳細については、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)を参照してください。
  
 **PR_MESSAGE_ATTACHMENTS**��g�p�ł��܂��B 
  
- **IMAPIProp::OpenProperty** ��A�Y�t�t�@�C���܂��͎�M�҂̃e�[�u���ɃA�N�Z�X���܂��B 
    
- **IMAPIProp::CopyTo** �܂��͏��O����A�܂��̓R�s�[����Ƃ��ɁA�Y�t�t�@�C����܂߂�ɂ́A **IMAPIProp::CopyProps** ���܂��B�ڍׂɂ��ẮA [IMAPIProp::CopyTo](imapiprop-copyto.md)��[IMAPIProp::CopyProps](imapiprop-copyprops.md)��Q�Ƃ��Ă��������B
    
- �q�̐����� [�Y�t�t�@�C���ɓK�p���邩��������ʐ������܂��B
    
�ڍׂɂ��ẮA [�Y�t�t�@�C���̃e�[�u��](attachment-tables.md)��Q�Ƃ��Ă��������B
  


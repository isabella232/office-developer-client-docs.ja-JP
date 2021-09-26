---
title: �쐬�ƃ��b�Z�[�W �X�g�A�Ń��b�Z�[�W��ۑ����܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a43569352cdcf8c0a8eac533be7a3b6cb7793652
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631007"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>メッセージ ストアのメッセージの作成と保存

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーが基盤となるストレージ メカニズムでメッセージの作成と保存を行う方法は、基盤となるストレージ メカニズムそのものに大きく依存します。一般的には、メッセージとその値のプロパティを保存するためのコードを記述するだけです。
  
メッセージ ストア プロバイダーが新しいメッセージを作成するときは、メッセージに必要なプロパティを付けてメッセージを作成する必要があります。これらのプロパティ一覧は、[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) インターフェイスの文書に記載されています。その後、クライアント アプリケーションが、[IMAPIProp](imapipropiunknown.md) メソッドを使ってすべての追加プロパティを追加します。 
  
When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.
  
MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called. 
  
���b�Z�[�W�̃I�u�W�F�N�g�̈ꕔ�̃v���p�e�B�ł́A���̂悤�ɁA **SaveChanges**���\�b�h�Ɋ֘A����N���C�A���g �A�v���P�[�V�����ɓ��ʂȈӖ�������܂��B 
  
- 一部のプロパティは、**SaveChanges** が呼び出される前に読み取り/書き込みが行われる必要がありますが、その後は読み取り専用になります。 たとえば、メッセージを作成する (つまり読み取り/書き込みである) クライアント アプリケーションによって、当初、**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) が設定されていても、いったん **SaveChanges** の呼び出しがあってからは変更できません。
    
- 一部のプロパティは、自らの属するフォルダーのプロパティ、または **IMAPIFolder** メソッドとの間で特別な関係を持っています。たとえば、**PR_MESSAGE_FLAGS** プロパティは、[IMAPIFolder::CreateMessage](imapifolder-createmessage.md) の呼び出しに使用されるフラグと関連があります。 
    
- 一部のプロパティは、**SaveChanges** が初めて呼び出されるまで使用できない場合があります。 たとえば、**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティは **SaveChanges** が初めて呼び出されるまで使用できない場合があります。 
    
- 一部のプロパティは、メッセージ オブジェクトのその他のプロパティと特別な関係を持っています。 たとえば、**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティは、通常、リッチ テキスト形式のメッセージをサポートするメッセージ ストア プロバイダーの **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティから派生します。
    
- 一部のプロパティは、メッセージ ストアに関連する複数のオブジェクト型で使用されます。 たとえば、**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティは、フォルダーでも、メッセージ オブジェクトでも、さらにはメッセージ ストア オブジェクトでも必要です。
    
メッセージ ストア プロバイダーには、このようなプロパティに対する適切なセマンティクスを実装する責任があります。
  
## <a name="see-also"></a>関連項目



[メッセージ ストアのメッセージの実装](implementing-messages-in-message-stores.md)


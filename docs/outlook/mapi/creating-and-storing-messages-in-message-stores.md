---
title: メッセージ ストアのメッセージの作成と保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589176"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>メッセージ ストアのメッセージの作成と保存

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーが基盤となるストレージ メカニズムでメッセージの作成と保存を行う方法は、基盤となるストレージ メカニズムそのものに大きく依存します。一般的には、メッセージとその値のプロパティを保存するためのコードを記述するだけです。
  
メッセージ ストア プロバイダーが新しいメッセージを作成するときは、メッセージに必要なプロパティを付けてメッセージを作成する必要があります。これらのプロパティ一覧は、[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)インターフェイスの文書に記載されています。その後、クライアント アプリケーションが、[IMAPIProp](imapipropiunknown.md)メソッドを使ってすべての追加プロパティを追加します。 
  
メッセージ ストア プロバイダーが基盤となるストレージ メカニズムにメッセージを保存するときは、メッセージのプロパティを繰り返し処理して、基盤となるストレージ メカニズムに保存する必要があります。そうすることで、後で開いたときにメッセージが完全な形で復元されます。
  
MAPI は[IMessage](imessageimapiprop.md)インターフェイス上のプロパティのトランザクションを要求します。つまり、プロパティに加えられた変更は、[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドがメッセージ オブジェクトに対して呼び出されるまでは永続的になりません。 メッセージ ストア プロバイダーには、この動作を実装する責任があります。 通常これは難しいことではなく、単に、プロパティが変更される間メモリ内でプロパティを保持し、**SaveChanges**が呼び出されたときに基盤となるストレージ メカニズムにプロパティをコミットすることを意味します。 
  
メッセージ オブジェクトのプロパティの中には、次に示すとおり、**SaveChanges**メソッドに関して、クライアント アプリケーションに対する特別なセマンティクスを持つものがあります。 
  
- 一部のプロパティは、**SaveChanges**が呼び出される前に読み取り/書き込みが行われる必要がありますが、その後は読み取り専用になります。 たとえば、メッセージを作成する (つまり読み取り/書き込みである) クライアント アプリケーションによって、当初、**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) が設定されていても、 いったん**SaveChanges**の呼び出しがあってからは変更できません。
    
- 一部のプロパティは、自らの属するフォルダーのプロパティ、または**IMAPIFolder**メソッドとの間で特別な関係を持っています。 たとえば、 **PR_MESSAGE_FLAGS**プロパティは、[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)の呼び出しに使用されるフラグと関連があります。 
    
- 一部のプロパティは、**SaveChanges**が初めて呼び出されるまで使用できない場合があります。 たとえば、**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティは**SaveChanges**が初めて呼び出されるまで使用できない場合があります。 
    
- 一部のプロパティは、メッセージ オブジェクトのその他のプロパティと特別な関係を持っています。 たとえば、**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティは、通常、リッチ テキスト形式をサポートするメッセージ ストア プロバイダーの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティから派生します。
    
- 一部のプロパティは、メッセージ ストアに関連する複数のオブジェクト型で使用されます。 たとえば、**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティは、フォルダーでも、メッセージ オブジェクトでも、さらにはメッセージ ストア オブジェクトでも必要です。
    
メッセージ ストア プロバイダーには、このようなプロパティに対する適切なセマンティクスを実装する責任があります。
  
## <a name="see-also"></a>関連項目



[メッセージ ストアのメッセージの実装](implementing-messages-in-message-stores.md)


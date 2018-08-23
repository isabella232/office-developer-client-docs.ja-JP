---
title: MAPI オブジェクトとプロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7ba58cc87b0eefe6c6ff70994d887d7f83e713b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592403"
---
# <a name="mapi-objects-and-properties"></a>MAPI オブジェクトとプロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
いくつかのプロパティは、多くの異なる種類のオブジェクトでサポートされます。 次のプロパティでは、複数のオブジェクトによって使用されるプロパティの例を示します。
  
- **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md)) は、オブジェクトを開くために使用するバイナリ識別子です。
    
- **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md)) は、オブジェクトの種類を識別する定数です。
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) は、ユーザーにオブジェクトの記述に使用される文字の文字列です。
    
その他のプロパティは、オブジェクトの 1 つの型の意味を確認します。 次のプロパティでは、1 種類のオブジェクトに適用されるプロパティの例を示します。
  
- **PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) は、メッセージの種類を説明するために使用する文字列です。
    
- **PR_ROWID**([PidTagRowid](pidtagrowid-canonical-property.md)) は、テーブル内の行を識別する整数です。
    
- **PR_ATTACH_SIZE**([PidTagAttachSize](pidtagattachsize-canonical-property.md)) は、添付ファイルのバイト数を格納する整数です。
    
その他のプロパティは、特定の状態のオブジェクトの 1 つの型にのみ適用。 この型のプロパティは、通常、メッセージのプロパティです。 メッセージが最初に作成されたときに、プロパティのセットが小さすぎます。 クライアントがメッセージング システムから受信者に送信される、メッセージの説明に必要なプロパティの数が増加します。 他のユーザーに表示されるだけ、メッセージとして送信されるときに送信されると、追加したプロパティの一部はメッセージにのみ表示されます。 メッセージでは、所属するクラスに関連付けられているプロパティもあります。 など、レポート メッセージは、注意のメッセージなど、他のクラスのメッセージではサポートされていないプロパティを持ちます。 
  
すべてのオブジェクトが必要なプロパティがいくつかと、その他の省略可能なプロパティがない可能性があります。 必要なプロパティはオブジェクトは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを使用して正常に保存する前にオブジェクト上に存在する必要があります。 クライアントまたはサービス プロバイダー オブジェクトを使用して、 **SaveChanges**の呼び出しの後必要なプロパティの可用性に依存できます。 これらのプロパティを取得するオブジェクトの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドまたは[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドへの呼び出しが成功することを確認することができます。 
  
省略可能なプロパティは、オブジェクトの実装では、によってまたは可能性のあるオブジェクトではサポートされていない可能性があります。 オブジェクトを使用して、クライアントまたはサービス プロバイダー オプションのプロパティ、 **GetProps**メソッドまたは**OpenProperty**メソッドを使用して有効な値に設定することは期待できません。 
  
一覧または [このプロパティの参照では、 [MAPI プロパティ](mapi-properties.md)を参照してください。 メッセージのそれぞれに属するプロパティの説明を格納し、アドレス帳オブジェクトがオブジェクトの標準的なインタ フェースの説明であります。 などのフォルダーのプロパティは、 **IMAPIFolder**で説明し、メッセージング ユーザーのプロパティは、 **IMailUser**で説明します。 レポート メッセージのプロパティを含む、メッセージのプロパティは、 **IMessage** [メッセージのプロパティの概要](message-properties-overview.md)を説明します。 テーブルのさまざまな種類のそれぞれに属するプロパティには、 [MAPI テーブル](mapi-tables.md)の該当するトピックが記載されています。 たとえば、[階層テーブル](hierarchy-tables.md)に階層テーブルのプロパティを示します。 フォームのサーバーに属するプロパティは[、フォームのプロパティの設定を選択する際](choosing-a-form-s-property-set.md)に説明します。
  
クライアントまたはサービス プロバイダーは、そのプロパティを取得するオブジェクトの**GetProps**メソッドを呼び出すし、これらのプロパティの 1 つは使用できません、 **GetProps**は MAPI_W_ERRORS_RETURNED の警告を返します。 呼び出しは、プロパティの一部が返されたために、成功すると見なされます。 クライアントまたはサービス プロバイダーの呼び出し**OpenProperty**とターゲット プロパティが使用できない場合は、メソッドは MAPI_E_NOT_FOUND のエラーで失敗します。 操作する前に、要求されたプロパティが返されることを確認するのには重要です。 
  
オブジェクトには、実装、およびプロパティを提供するサービス プロバイダー プロパティが読み取り/書き込みまたは読み取り専用のアクセス許可。 読み取り/書き込みのアクセス許可により、その値を変更するのにはプロパティを使用して、クライアントまたはサービス プロバイダー読み取り専用のアクセス許可により、サービス プロバイダーのみオブジェクトを所有している変更を加える。 
  
正確には、現在に設定するプロパティ オブジェクトを調べるには、 [IMAPIProp::GetPropList](imapiprop-getproplist.md)を呼び出します。 **Getproplist メソッド**のメソッドは、呼び出し元が存在しない可能性のあるプロパティを開こうとしてが行われる前に使用可能なアウトを見つけることができます。 標準の一連の特定の種類のすべてのオブジェクトをサポートしているプロパティがないため、オブジェクトが特定のプロパティをサポートしているかどうかを推測することはできません。 推測作業を排除する**getproplist メソッド**を呼び出すことです。 
  
## <a name="see-also"></a>関連項目



[MAPI オブジェクトとプロパティ](mapi-objects-and-properties.md)


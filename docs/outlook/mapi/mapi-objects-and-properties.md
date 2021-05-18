---
title: MAPI オブジェクトとプロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7fef84b7519c7a9d6373198283e903fba4fd0780
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411212"
---
# <a name="mapi-objects-and-properties"></a>MAPI オブジェクトとプロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のプロパティは、さまざまな種類のオブジェクトでサポートされています。 次のプロパティは、複数のオブジェクトで使用されるプロパティの例です。
  
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) は、オブジェクトを開くために使用されるバイナリ識別子です。
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) は、オブジェクトの種類を識別するために使用される定数です。
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) は、ユーザーにオブジェクトを記述するために使用される文字列です。
    
他のプロパティは、単一の種類のオブジェクトに対して意味があります。 次のプロパティは、1 種類のオブジェクトに適用されるプロパティの例です。
  
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) は、メッセージの種類を記述するために使用される文字列です。
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) は、テーブル内の行を識別するために使用される整数です。
    
- **PR_ATTACH_SIZE** ([PidTagAttachSize](pidtagattachsize-canonical-property.md)) は、添付ファイルにバイト数を格納するために使用される整数です。
    
その他のプロパティは、特定の状態にある 1 種類のオブジェクトにのみ適用できます。 この種類のプロパティは、通常、メッセージのプロパティです。 メッセージが最初に作成されると、そのプロパティのセットは非常に小さくてすみます。 クライアントがメッセージング システムを介して受信者に送信すると、メッセージを記述するために必要なプロパティの数が増える。 これらの追加されたプロパティの一部は、配信中のメッセージにのみ表示され、他のプロパティは送信中のメッセージにのみ表示されます。 メッセージには、所属するクラスに関連付けられているプロパティも含まれます。 たとえば、レポート メッセージには、メモ メッセージなどの他のクラスのメッセージでサポートされていないプロパティがあります。 
  
すべてのオブジェクトには必要なプロパティがいくつか含め、その他のオプション プロパティを持つ場合とそうでない場合があります。 必要なプロパティは、オブジェクトが [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドで正常に保存される前にオブジェクトに存在する必要があるプロパティです。 オブジェクトを使用するクライアントまたはサービス プロバイダーは **、SaveChanges** 呼び出し後に必要なプロパティの可用性によって異なります。 つまり、これらのプロパティを取得するために、オブジェクトの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドまたは [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドの呼び出しが成功する可能性があります。 
  
省略可能なプロパティは、オブジェクトの実装者に応じて、オブジェクトでサポートされる場合とサポートされない可能性があるプロパティです。 オブジェクトを使用するクライアントまたはサービス プロバイダーは、オプションのプロパティを **GetProps** メソッドまたは **OpenProperty** メソッドを使用して使用し、有効な値に設定することはできません。 
  
このリファレンスのリストまたはプロパティについては、「MAPI プロパティ」 [を参照してください](mapi-properties.md)。 各メッセージ ストアオブジェクトとアドレス帳オブジェクトに属するプロパティの説明については、オブジェクトの標準インターフェイスの説明を参照してください。 たとえば、フォルダーのプロパティについては **IMAPIFolder** で説明し、メッセージング ユーザーのプロパティについては **IMailUser で説明します**。 レポート メッセージのプロパティを含むメッセージ プロパティについては **、「IMessage」** および「メッセージ プロパティ [の概要」で説明します](message-properties-overview.md)。 各種類のテーブルに属するプロパティについては、適切な MAPI テーブルのトピック [で説明](mapi-tables.md) します。 たとえば、階層テーブルのプロパティについては、「階層テーブル」 [で説明します](hierarchy-tables.md)。 フォーム サーバーに属するプロパティは、「フォームのプロパティ セットの選択」 [で説明しています](choosing-a-form-s-property-set.md)。
  
クライアントまたはサービス プロバイダーがオブジェクトの **GetProps** メソッドを呼び出して、いくつかのプロパティを取得し、これらのプロパティの 1 つを使用できない場合 **、GetProps** は警告メッセージをMAPI_W_ERRORS_RETURNED。 一部のプロパティが返されたため、呼び出しは成功したと見なされます。 クライアントまたはサービス プロバイダーが **OpenProperty** を呼び出し、ターゲット プロパティを使用できない場合、メソッドはエラー メッセージでMAPI_E_NOT_FOUND。 操作を試みる前に、要求されたプロパティが返されるのを確認することが重要です。 
  
オブジェクト、実装を提供するサービス プロバイダー、およびプロパティに応じて、プロパティは読み取り/書き込みまたは読み取り専用のアクセス許可を持つ場合があります。 読み取り/書き込みアクセス許可を使用すると、プロパティを使用するクライアントまたはサービス プロバイダーが値を変更できます。読み取り専用アクセス許可を使用すると、オブジェクトを所有するサービス プロバイダーだけが変更を行えます。 
  
オブジェクトに現在設定されているプロパティを正確に確認するには [、IMAPIProp::GetPropList を呼び出します](imapiprop-getproplist.md)。 **GetPropList メソッドを** 使用すると、呼び出し元は、存在しない可能性のあるプロパティを開く前に使用可能な情報を見つけることができます。 特定の型のすべてのオブジェクトがサポートするプロパティの標準セットはないので、オブジェクトが特定のプロパティをサポートするかどうかを推測することは不可能です。 **GetPropList を呼び出** すと、推測作業が不要です。 
  
## <a name="see-also"></a>関連項目



[MAPI オブジェクトとプロパティ](mapi-objects-and-properties.md)


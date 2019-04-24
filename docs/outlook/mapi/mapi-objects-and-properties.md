---
title: MAPI のオブジェクトとプロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0aebf536-dcfb-406d-86ac-65db98c78139
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7fef84b7519c7a9d6373198283e903fba4fd0780
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345809"
---
# <a name="mapi-objects-and-properties"></a>MAPI のオブジェクトとプロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティによっては、さまざまな種類のオブジェクトでサポートされています。 次のプロパティは、複数のオブジェクトで使用されるプロパティの例です。
  
- **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md)) は、オブジェクトを開くために使用されるバイナリ識別子です。
    
- **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md)) は、オブジェクトの種類を識別するために使用される定数です。
    
- **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) は、ユーザーにオブジェクトを記述するために使用される文字列です。
    
オブジェクトの種類によっては、その他のプロパティが適しています。 次のプロパティは、1つの種類のオブジェクトに適用されるプロパティの例です。
  
- **PR_MESSAGE_CLASS**([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) は、メッセージの種類を表すために使用される文字列です。
    
- **PR_ROWID**([PidTagRowid](pidtagrowid-canonical-property.md)) は、テーブル内の行を識別するために使用される整数です。
    
- **PR_ATTACH_SIZE**([PidTagAttachSize](pidtagattachsize-canonical-property.md)) は、添付ファイル内のバイト数を格納するために使用される整数です。
    
その他のプロパティは、特定の状態にある1つの種類のオブジェクトに対してのみ適用されます。 この型のプロパティは、通常、メッセージプロパティです。 最初にメッセージを作成すると、そのプロパティのセットは非常に小さくなります。 メッセージングシステムによってクライアントによって受信者に送信されると、メッセージを説明するために必要なプロパティの数が増加します。 これらの追加プロパティの一部は、メッセージが配信されるときにのみ表示されますが、送信されるメッセージのみに表示されるものもあります。 メッセージには、それが属するクラスに関連付けられたプロパティもあります。 たとえば、レポートメッセージには、メモメッセージなど、他のクラスのメッセージではサポートされていないプロパティがあります。 
  
すべてのオブジェクトには、いくつかの必要なプロパティがあり、その他のオプションのプロパティが存在する場合もあります。 必須のプロパティは、オブジェクトを[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを使用して正常に保存できるようにするために、オブジェクトに存在する必要があるプロパティです。 オブジェクトを使用するクライアントまたはサービスプロバイダーは、 **SaveChanges**呼び出しの後に必要なプロパティが使用可能かどうかによって決まります。 つまり、これらのプロパティを取得するオブジェクトの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドまたは[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドの呼び出しが成功することを確認できます。 
  
省略可能なプロパティは、オブジェクトの実装によっては、オブジェクトによってサポートされるかもしれませんが、プロパティです。 オブジェクトを使用するクライアントまたはサービスプロバイダーは、 **GetProps**または**openproperty**メソッドを通じてオプションのプロパティを使用でき、有効な値に設定することを想定できません。 
  
この参照のリストまたはプロパティについては、「 [MAPI のプロパティ](mapi-properties.md)」を参照してください。 各メッセージストアおよびアドレス帳オブジェクトに属するプロパティについては、そのオブジェクトの標準インターフェイスに関する説明を参照してください。 たとえば、フォルダーのプロパティについては**imapifolder**を使用し、メッセージングユーザーのプロパティについては、 **imailuser**を使用して説明します。 メッセージプロパティ (レポートメッセージプロパティなど) については、「 **IMessage** 」および「[メッセージプロパティの概要](message-properties-overview.md)」を参照してください。 それぞれの種類のテーブルに属するプロパティについては、該当する[MAPI テーブル](mapi-tables.md)のトピックを参照してください。 たとえば、階層テーブルのプロパティについては、「[階層テーブル](hierarchy-tables.md)」を参照してください。 フォーム[のプロパティセットの選択](choosing-a-form-s-property-set.md)については、フォームサーバーに属するプロパティについて説明します。
  
クライアントまたはサービスプロバイダーがオブジェクトの**GetProps**メソッドを呼び出して、そのプロパティのいくつかを取得しようとしたときに、これらのプロパティのいずれかが使用できない場合、 **GetProps**は警告 MAPI_W_ERRORS_RETURNED を返します。 一部のプロパティが返されたため、呼び出しは成功したと見なされます。 クライアントまたはサービスプロバイダーが**openproperty**を呼び出したときに、target プロパティが使用できない場合、このメソッドはエラー MAPI_E_NOT_FOUND で失敗します。 要求されたプロパティが返されたことを確認してから、操作を実行することが重要です。 
  
実装を提供するサービスプロバイダー、およびプロパティであるプロパティに応じて、プロパティは読み取り/書き込み可能または読み取り専用のアクセス許可を持つことができます。 読み取り/書き込みアクセス許可は、クライアントまたはサービスプロバイダーがプロパティを使用してその値を変更できるようにします。読み取り専用のアクセス許可では、オブジェクトを所有しているサービスプロバイダーのみが変更を行うことができます。 
  
オブジェクトに現在設定されているプロパティを正確に確認するには、 [imapiprop:: getproplist](imapiprop-getproplist.md)を呼び出します。 **getproplist**メソッドを使用すると、存在しない可能性のあるプロパティを開こうとしているときに、使用可能なものを発信者が検出できます。 特定の型のすべてのオブジェクトがサポートするプロパティの標準セットが存在しないため、オブジェクトが特定のプロパティをサポートしているかどうかを推測することはできません。 **getproplist**を呼び出すと、その推測は行われなくなります。 
  
## <a name="see-also"></a>関連項目



[MAPI のオブジェクトとプロパティ](mapi-objects-and-properties.md)


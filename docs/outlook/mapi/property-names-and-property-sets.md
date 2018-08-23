---
title: プロパティ名とプロパティ セット
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0272464d9a397f169b27aa15c80a17b49a3e9977
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571830"
---
# <a name="property-names-and-property-sets"></a>プロパティ名とプロパティ セット

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
すべての名前付きプロパティの名前には、2 つの部分があります。
  
- グローバルに一意の識別子または GUID では、プロパティ セットを指定します。
    
- Unicode 文字の文字列、または 32 ビットの数値です。 
    
[MAPINAMEID](mapinameid.md)構造体を使用して、名前付きプロパティの名前を説明します。 この構造体には、プロパティ セットのメンバー、メンバーの名前を指定する数値または文字列のいずれかの形式でどちらの形式が使用される特定のメンバーが含まれています。 プロパティ セット、プロパティ名の一部であるために、省略可能なことはできません。 MAPI には、クライアントとサービス ・ プロバイダーで使用するためのいくつかのプロパティ セットが定義されているが、既存のプロパティ セットが適切でない場合は、新しいプロパティ セットを定義できます。 クライアントとサービス ・ プロバイダーは、 [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx)関数を呼び出すことによって、独自のプロパティ セットを定義できます。 通常これらのプロパティ セットは、カスタム クライアント アプリケーションの作成されます。 
  
MAPI のプロパティ セットは、次の定数によって表されます。
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_MAPI プロパティ セットは予約されています。名前付きプロパティの範囲の下の識別子を持つプロパティの名前を生成するサービス プロバイダーによって使用されます。 PS_PUBLIC_STRINGS プロパティ セットは、IPM メッセージの名前付きプロパティをクライアントによって使用されます。 PS_PUBLIC_STRINGS プロパティ セットの名前付きプロパティがあるためにという名前のプロパティをこのプロパティを設定を非表示のメッセージを作成しないように IPC メッセージ クラスに属している必要があります次のようにクライアントのユーザー インターフェイスで表示します。 代わりに、メッセージ クラスに固有の範囲、0x7FFF を 0x6800 にプロパティを作成する必要があります。
  
その他のプロパティ セットは、通常のルーティングの一覧のメンバーである受信者を説明する名前付きのプロパティを保持します。 同じ種類の受信者のリストのプロパティに関連付けられているプロパティの情報を含む、これらのプロパティ セットにプロパティが理解ゲートウェイ メッセージング システムのターゲットのマッピングを必要とします。 5 種類のプロパティを記述するための情報があるため、MAPI が 5 つの異なるプロパティ セットを定義します。 メッセージのルーティングの一覧のメンバーのアドレスおよびアドレス タイプを含める必要があります PS_ROUTING_EMAIL_ADDRESSES 内の各メンバーの名前付きプロパティと PS_ROUTING_ADDRTYPE プロパティの割り当てを送信するクライアントを設定します。 これにより、アドレスとアドレスの種類は外部のメッセージング システムに送信されるときに実行可能なことです。
  
## <a name="see-also"></a>関連項目



[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)


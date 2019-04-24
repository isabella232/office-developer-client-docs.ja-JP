---
title: プロパティ名とプロパティセット
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328547"
---
# <a name="property-names-and-property-sets"></a>プロパティ名とプロパティセット

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべての名前付きプロパティの名前は、2つの部分で構成されます。
  
- プロパティセットを指定するグローバル一意識別子 (GUID)。
    
- Unicode 文字列または32ビットの数値を指定します。 
    
名前付きプロパティの名前については、 [mapinameid](mapinameid.md)構造を使用して説明します。 この構造体には、プロパティセットメンバー、数値または文字列形式のいずれかの名前を指定するメンバ、および使用する形式を識別するメンバが含まれています。 プロパティセットはプロパティの名前の一部であるため、オプションではありません。 MAPI では、クライアントとサービスプロバイダーが使用するためにいくつかのプロパティセットが定義されていますが、既存のプロパティセットが適切でない場合は、新しいプロパティセットを定義できます。 クライアントおよびサービスプロバイダーは、 [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx)関数を呼び出すことによって、独自のプロパティセットを定義できます。 通常、これらのプロパティセットはカスタムクライアントアプリケーション用に作成されます。 
  
MAPI のプロパティセットは、次の定数で表されます。
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_MAPI プロパティセットは予約されています。このメソッドは、名前付きプロパティの範囲の下に識別子を持つプロパティの名前を生成するために、サービスプロバイダーによって使用されます。 PS_PUBLIC_STRINGS プロパティセットは、IPM メッセージの名前付きプロパティのクライアントによって使用されます。 PS_PUBLIC_STRINGS プロパティセットの名前付きプロパティはクライアントのユーザーインターフェイスに表示されるため、IPC メッセージクラスに属するものなどの非表示のメッセージは、このプロパティセットで名前付きプロパティを作成しないようにしてください。 代わりに、メッセージクラス固有の範囲である 0x6800 ~ で、プロパティを作成する必要があります。
  
その他のプロパティセットは、通常、ルーティングリストのメンバーである受信者を説明する名前付きプロパティを保持します。 受信者リストのプロパティに関連付けられているプロパティと同じ種類の情報が含まれている場合、これらのプロパティセットのプロパティは、対象のメッセージングシステムへのマッピングを要求するためにゲートウェイによって認識されます。 プロパティを説明するための情報には5つの種類があるため、MAPI は5つの異なるプロパティセットを定義しています。 ルーティングリストのメンバーのアドレスとアドレスの種類が含まれている必要があるメッセージを送信するクライアントは、PS_ROUTING_EMAIL_ADDRESSES プロパティと PS_ROUTING_ADDRTYPE プロパティセットの各メンバーに対して名前付きプロパティを割り当てます。 これにより、外部メッセージングシステムに送信するときに、アドレスとアドレスの種類が引き続き有効になります。
  
## <a name="see-also"></a>関連項目



[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)


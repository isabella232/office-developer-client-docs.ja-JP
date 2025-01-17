---
title: クライアントの名前付け責任
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: de707abc99393d40461e0f2be696040b570764d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584690"
---
# <a name="client-naming-responsibilities"></a>クライアントの名前付け責任

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、ゲートウェイによって変換する必要があるプロパティの名前付け規則に従う必要があります。 変換するプロパティはすべて、マップ可能なプロパティを保持するために指定された 5 つのプロパティ セットの 1 つで名前付きプロパティとして作成する必要があります。
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
同じユーザーに関連するアドレス指定プロパティには、同じ名前を付ける必要があります。 ゲートウェイは、この名前付け規則に依存しています。これにより、アドレスと正しいアドレスの種類を一致できます。 アドレス解析では、アドレスとアドレスの種類の間のマッピングが正確である必要があります。
  
MAPI 名前付きプロパティは **MAPINAMEID** データ構造で表され、プロパティ名は Unicode 文字列または 32 ビット整数のいずれかになります。 詳細については [、「MAPINAMEID」を参照してください](mapinameid.md)。 アドレスのグループには、マップ可能なプロパティのセットを区別する簡単な方法であり、ユーザーに対するインデックスとして簡単に機能することができるため、整数の名前付けをお勧めします。 整数を使用する代わりに、1 つの文字列をユーザーのマップ可能なプロパティの 5 つすべての名前として割り当てる方法があります。 マッピングが必要なユーザーが 1 人だけである場合、文字列の割り当ては受け入れ可能です。 ただし、複数のユーザーがある場合は、整数の名前付けを使用する方が良いです。 名前は、数値または文字列ベースのどちらでも、メッセージ クラス固有のプロパティまたはクライアント アプリケーションによって定義されたプロパティ セットに属するプロパティに格納する必要があります。 
  
> [!NOTE]
> 整数名を文字列 ("route_recipient_1" や "route_recipient_2" に変換しないようにします。 この作業は不要です。 
  
この名前付け規則の動作を説明するには、4 人チームの各メンバーにメッセージを送信するルーティング アプリケーションを検討してください。 1 人のメンバーがメッセージを受信すると、そのメッセージに応答してから、コンパイルされた応答を次のメンバーに送信する必要があります。 元のメッセージには、チームの最初のメンバーという 1 つのエントリを含む受信者リストが含まれる。 メッセージ内に埋め込まれているのは、他の 3 人のチーム メンバーのゲートウェイマップ可能なプロパティです。 各メンバーには、ゲートウェイマップ可能なプロパティ セットに存在する 5 つのコア ユーザー プロパティがあります。このプロパティには、名前として一意の番号が割り当てられます。 
  
次の表は、最初のチーム メンバーが終了するとメッセージがルーティングされる残りの 3 人のチーム メンバーに対して格納されているゲートウェイマップ可能なプロパティのセットごとに設定を示しています。
  
|**Property Set**|**2  <br/> 番目のチーム メンバー**|**サード チーム  <br/> メンバー**|**4 番目の  <br/> チーム メンバー**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |アドレス = 0  <br/> |アドレス = 1  <br/> |アドレス = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |アドレスの種類 = 0  <br/> |アドレスの種類 = 1  <br/> |アドレスの種類 = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |表示名 = 0  <br/> |表示名 = 1  <br/> |表示名 = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |エントリ識別子 = 0  <br/> |エントリ識別子 = 1  <br/> |エントリ識別子 = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |検索キー = 0  <br/> |検索キー = 1  <br/> |検索キー = 2  <br/> |
   
マップ可能な検索キーを他のメッセージ プロパティへの参照として使用するクライアントは、マップ可能なプロパティ セットの 1 つに配置しない限り、他のメッセージ プロパティは変換されないと認識する必要があります。 マップされた検索キーへのマップされていない参照を持つメッセージが別のメッセージング ドメインの宛先に送信される場合、参照は無効です。 これらの他のプロパティを検索キーとの同期を維持するには、PS_ROUTING_SEARCH_KEY プロパティ セットに文字列名を割り当て、マップ可能なコア プロパティに指定された名前を妨げない名前を割り当てることができます。 たとえば、クライアントが長いルーティング リストの最後のユーザーの検索キーを含むプロパティを送信する必要がある場合です。 クライアントは、"PS_ROUTING_SEARCH_KEY" という名前のプロパティ セットに名前付きプロパティをlast_search_key。 マップ可能なプロパティ セットに格納されるので、"last_search_key" プロパティはゲートウェイマップ可能なプロパティの残りの部分と共に変換されます。
  


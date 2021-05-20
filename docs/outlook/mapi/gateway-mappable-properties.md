---
title: ゲートウェイ マッピング可能プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430477"
---
# <a name="gateway-mappable-properties"></a>ゲートウェイ マッピング可能プロパティ

**適用対象**: Outlook 2013 | Outlook 2016 
  
Gateway-mappable プロパティは、あるメッセージング ドメインから別のメッセージング ドメインに送信するときに変換が必要なプロパティです。 MAPI のゲートウェイマップ可能プロパティを使用すると、メッセージにゲートウェイを必要とする情報を含め、宛先メッセージング システムが適切に使用できます。 ゲートウェイ開発者は、この変換機能を提供する必要はありませんが、ゲートウェイマップ可能なプロパティを、メッセージ コンテンツの処理を改善する機会と考える必要があります。
  
MAPI では、ゲートウェイマップ可能なプロパティの 5 種類を指定します。
  
- 表示名
    
- 電子メール アドレス
    
- メールの種類
    
- エントリ識別子
    
- 検索キー
    
これは、受信者、送信者、レポート受信者、委任された送信者と受信者に関連付けられているアドレス指定プロパティのセットです。 ゲートウェイがそれらを特別に処理するために、クライアントがこれらのプロパティを定義するために、MAPI は名前付きプロパティとプロパティ セットを使用して名前付き規則を指定します。 名前付きプロパティ、マッピングを必要とするアドレス指定プロパティを保持する 5 つのプロパティ セットが存在します。 mappable プロパティの種類ごとに 1 つのプロパティ セットがあります。 これらの名前付きアドレス指定プロパティを保持するプロパティ セットは次のとおりです。
  
|**プロパティ セット**|**説明**|
|:-----|:-----|
|PS_ROUTING_DISPLAY_NAME  <br/> |表示名として使用される文字列プロパティが含まれます。  <br/> |
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |電子メール アドレスとして使用される文字列プロパティが含まれます。  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |電子メール アドレスの種類として使用される文字列プロパティが含まれます。  <br/> |
|PS_ROUTING_ENTRYID  <br/> |長期エントリ識別子として使用されるバイナリ プロパティを含む。  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |検索キーとして使用されるバイナリ プロパティが含まれる。  <br/> |
   


---
title: MAPI ユーティリティの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1c2ac40be8e0928e92e2f483c236f42ae8a0ee9c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566221"
---
# <a name="using-the-mapi-utilities"></a>MAPI ユーティリティの使用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI ユーティリティは、テーブル データとプロパティ データ オブジェクトと、その他の機能をサポートするさまざまな機能でででています。 クライアントがこれらのユーティリティのみを必要とし、MAPI サブシステムにログオンしてサービス プロバイダーとの接続を確立する必要が生じ得る可能性があります。 クライアントがこのカテゴリに適合する場合は、初期化時に[MAPIInitialize](mapiinitialize.md)関数ではなく API 関数[ScInitMapiUtil](scinitmapiutil.md)を呼び出します。 
  
 **ScInitMapiUtil を使用** すると、クライアントは MAPI アロケーターを必要とするユーティリティ関数を使用できますが、割り当て子を明示的に要求することはできません。 シャットダウンする時間が近い場合は [、DEinitMapiUtil](deinitmapiutil.md) を呼び出して [、MAPIUninitialize ではなくリソースを解放します](mapiuninitialize.md)。 **MAPIInitialize を呼び出さないクライアントは****、MAPIUninitialize を呼び出す必要があります**。
  
**MAPIInitialize** ではなく **ScInitMapiUtil** を呼び出し **、IMAPITable** メソッドではなく **ITableData** メソッドを使用してテーブルを使用している場合は、テーブル通知は機能しません。 通知には、MAPI ライブラリと [IMAPITable : IUnknown の使用が必要です](imapitableiunknown.md)。
  


---
title: MAPI ユーティリティの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409987"
---
# <a name="using-the-mapi-utilities"></a>MAPI ユーティリティの使用

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI ユーティリティは、テーブル データとプロパティ データ オブジェクトと、その他の機能をサポートするさまざまな機能でででています。 クライアントがこれらのユーティリティのみを必要とし、MAPI サブシステムにログオンしてサービス プロバイダーとの接続を確立する必要が生じ得る可能性があります。 クライアントがこのカテゴリに適合する場合は、初期化時に[MAPIInitialize](mapiinitialize.md)関数ではなく API 関数[ScInitMapiUtil](scinitmapiutil.md)を呼び出します。 
  
 **ScInitMapiUtil を使用** すると、クライアントは MAPI アロケーターを必要とするユーティリティ関数を使用できますが、割り当て子を明示的に要求することはできません。 シャットダウンする時間が近い場合は [、DEinitMapiUtil](deinitmapiutil.md) を呼び出して [、MAPIUninitialize ではなくリソースを解放します](mapiuninitialize.md)。 **MAPIInitialize を呼び出さないクライアントは****、MAPIUninitialize を呼び出す必要があります**。
  
**MAPIInitialize** ではなく **ScInitMapiUtil** を呼び出し **、IMAPITable** メソッドではなく **ITableData** メソッドを使用してテーブルを使用している場合は、テーブル通知は機能しません。 通知には、MAPI ライブラリと [IMAPITable : IUnknown の使用が必要です](imapitableiunknown.md)。
  


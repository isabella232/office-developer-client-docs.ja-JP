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
  
MAPI ユーティリティは、テーブルデータオブジェクトとプロパティデータオブジェクト、およびその他の機能をサポートするさまざまな機能で構成されています。 クライアントはこれらのユーティリティのみを必要とすることができ、サービスプロバイダーとの接続を確立するために MAPI サブシステムにログオンする必要はありません。 クライアントがこのカテゴリに適合する場合は、初期化時に[MAPIInitialize](mapiinitialize.md)関数ではなく[ScInitMapiUtil](scinitmapiutil.md) API 関数を呼び出します。 
  
 **ScInitMapiUtil**では、クライアントが MAPI allocators を必要とするユーティリティ関数を使用できますが、allocators は明示的には要求しません。 シャットダウンする時間がある場合は、 [DeinitMapiUtil](deinitmapiutil.md)を呼び出して、 [MAPIUninitialize](mapiuninitialize.md)ではなくリソースを解放します。 **MAPIInitialize**を呼び出さないクライアントは、 **MAPIUninitialize**を呼び出すことはできません。
  
**MAPIInitialize**ではなく**ScInitMapiUtil**を呼び出し、 **IMAPITable**メソッドを使用するのではなく、 **itabledata**メソッドを使用してテーブルを使用している場合は、テーブル通知が機能しないことに注意してください。 通知には、MAPI ライブラリと[IMAPITable: IUnknown](imapitableiunknown.md)を使用する必要があります。
  


---
title: MAPI ユーティリティの初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420949"
---
# <a name="initializing-the-mapi-utilities"></a>MAPI ユーティリティの初期化

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
使用する必要がある MAPI の唯一の部分がユーティリティである場合は、MAPI の MAPIUTIL で宣言されているインターフェイスと関数です。IPropData や **ITableData** などの **H** ヘッダー ファイルは、初期化のために **MAPIInitialize を** 呼び出す必要があります。 詳細については [、「IPropData : IMAPIProp](ipropdataimapiprop.md) [、ITableData :](itabledataiunknown.md)IUnknown、MAPIInitialize」 [を参照してください](mapiinitialize.md)。 代わりに **、ScInitMapiUtil 関数を呼び出** します。 詳細については [、「ScInitMapiUtil」を参照してください](scinitmapiutil.md)。 **ScInitMapiUtil** を使用すると、クライアント アプリケーションは、MAPI アロケーターを必要とするが、明示的に要求しないユーティリティ関数とメソッドを使用できます。 
  
シャットダウン時に **DeinitMapiUtil** を呼び出して、ユーティリティに接続されているリソースを解放します。 **MAPIUninitialize を呼び出さない**。 詳細については[、「DeinitMapiUtil」および](deinitmapiutil.md)[「MAPIUninitialize」を参照してください](mapiuninitialize.md)。
  
ITableData インターフェイスは **、MAPIInitialize** ではなく **ScInitMapiUtil** を呼び出したクライアントのテーブル通知をサポートしません。  
  


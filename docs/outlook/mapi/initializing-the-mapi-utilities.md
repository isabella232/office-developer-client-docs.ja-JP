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
  
使用する必要がある mapi の部分が、mapi の MAPIUTIL で宣言されているインターフェイスと関数である場合があります。H ヘッダーファイル ( **ipropdata**や**itabledata**など) — **MAPIInitialize**を呼び出して初期化する必要はありません。 詳細については、「 [ipropdata: imapiprop](ipropdataimapiprop.md)」、「 [itabledata: IUnknown](itabledataiunknown.md)」、および「 [MAPIInitialize](mapiinitialize.md)」を参照してください。 代わりに、 **ScInitMapiUtil**関数を呼び出します。 詳細については、「 [ScInitMapiUtil](scinitmapiutil.md)」を参照してください。 **ScInitMapiUtil**では、クライアントアプリケーションが MAPI allocators を必要とするユーティリティ関数およびメソッドを使用できますが、それらを明示的には要求しません。 
  
シャットダウン時に、 **DeinitMapiUtil**を呼び出して、ユーティリティに接続されているリソースを解放します。 **MAPIUninitialize**は呼び出さないでください。 詳細については、「 [DeinitMapiUtil](deinitmapiutil.md) 」と「 [MAPIUninitialize](mapiuninitialize.md)」を参照してください。
  
**itabledata**インターフェイスは、 **MAPIInitialize**ではなく**ScInitMapiUtil**を呼び出したクライアントのテーブル通知をサポートしていないことに注意してください。 
  


---
title: エラー処理の戦略
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424148"
---
# <a name="strategies-for-error-handling"></a>エラー処理の戦略

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
インターフェイス メソッドは仮想メソッドなので、呼び出し元として、任意の 1 つの呼び出しから返される値の完全なセットを知る必要があります。 メソッドの実装の 1 つは、5 つの値を返す場合があります。別のユーザーが 8 を返す場合があります。 MAPI ドキュメントの参照エントリには、メソッドごとに返される値がいくつか一覧表示されます。これらは、クライアントまたはサービス プロバイダーが特別な意味を持つため、チェックして処理できる値です。 他の値を返す場合がありますが、意味がありませんので、それを処理する特別なコードは必要ありません。 成功または失敗の簡単なチェックが適切です。
  
インターフェイス メソッドのいくつかは、警告を返します。 クライアントまたはサービス プロバイダーが呼び出すメソッドが警告を返す場合は **、HR_FAILED** マクロを使用して、ゼロまたは 0 以外のチェックではなく、戻り値をテストします。 警告は 0 以外の値ですが、ハイ ビット が設定されていないという点でエラー コードとは異なります。 クライアントまたはサービス プロバイダーがマクロを使用しない場合は、警告がエラーと間違えられる可能性があります。 
  
ほとんどのインターフェイス メソッドと関数は HRESULT 値を返しますが、一部の関数は符号なし長整数型 (long) の値を返します。 また、MAPI 環境で使用される一部のメソッドは、COM から取得され、MAPI エラー値ではなく COM エラー値を返します。 通話を行う場合は、次のガイドラインに注意してください。
  
- **IUnknown::AddRef** または **IUnknown::Release** の戻り値に依存したり使用したりすることはできません。 これらの戻り値は、診断のみを目的とします。 
    
- **IUnknown::QueryInterface** は、MAPI エラーではなく、FACILITY_NULLまたはFACILITY_RPC一般的な COM エラーを返します。 
    
- その他のすべてのインターフェイス メソッドは、MAPI インターフェイス エラーを返し、FACILITY_ITF、FACILITY_RPCエラー FACILITY_NULL返します。
    
サポートされていない MAPI メソッドを呼び出す場合、次の 4 つのエラーのいずれかを返します。 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION。 
  


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327217"
---
# <a name="strategies-for-error-handling"></a>エラー処理の戦略

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
インターフェイスメソッドは仮想になっているため、呼び出し元として、1つの呼び出しから返される可能性のある値の完全なセットを知ることはできません。 1つのメソッドの実装は5つの値を返す場合があります。別の場合は8を返します。 MAPI ドキュメントの参照エントリには、各メソッドに対して返すことができるいくつかの値が記載されています。これらの値は、クライアントまたはサービスプロバイダーが特別な意味を持つため、確認して処理することができます。 その他の値は返すことができますが、意味がないため、これらを処理するための特別なコードは必要ありません。 成功または失敗の簡単なチェックは、十分です。
  
インターフェイスメソッドのいくつかは、警告を返します。 クライアントまたはサービスプロバイダーが呼び出すメソッドが警告を返す場合は、 **HR_FAILED**マクロを使用して、ゼロまたは0以外のチェックではなく、戻り値をテストします。 警告は、0以外の場合でも、上位ビットが設定されていないというエラーコードとは異なります。 クライアントまたはサービスプロバイダーがマクロを使用しない場合は、エラーの原因となる警告が表示されることがあります。 
  
ほとんどのインターフェイスメソッドと関数は、HRESULT 値を返しますが、一部の関数は、符号なし長整数型 (long) の値を返します。 また、mapi 環境で使用されているいくつかのメソッドは、com からのものであり、mapi エラー値ではなく com エラー値を返します。 呼び出しを行うときは、次のガイドラインに注意してください。
  
- **iunknown:: AddRef**または**iunknown:: Release**の戻り値を使用したり、使用したりすることはありません。 これらの戻り値は、診断のみを目的としています。 
    
- **IUnknown:: QueryInterface**は、MAPI エラーではなく、ファシリティが FACILITY_NULL または FACILITY_RPC である汎用 COM エラーを常に返します。 
    
- 他のすべてのインターフェイスメソッドは、FACILITY_ITF のファシリティ、FACILITY_RPC、または FACILITY_NULL のエラーを含む MAPI インターフェイスエラーを返します。
    
サポートされていない MAPI メソッドに対して呼び出しを行った場合、次の4つのエラーのいずれかが返されることがあります。 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION。 
  


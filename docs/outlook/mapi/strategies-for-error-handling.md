---
title: エラー処理のための戦略
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804014"
---
# <a name="strategies-for-error-handling"></a>エラー処理のための戦略

  
  
**適用されます**: Outlook 
  
インターフェイス メソッドは仮想であるため、1 つの呼び出しから返される値の完全なセットを呼び出し元として認識することはできません。 メソッドの実装の 1 つが 5 つの値を返す可能性があります。別、8 つを返すことがあります。 MAPI ドキュメント内の参照エントリは、各メソッドに返すことができるいくつかの値を一覧表示します。これらは、クライアントまたはサービス プロバイダーが確認し、特別な意味を持っているために処理される値です。 その他の値を返すことができますが、意味のあるできないため、それらを処理するために特別なコードが必要ではありません。 成功または失敗の簡単なチェックで十分です。
  
インターフェイスのメソッドのいくつかは、警告を返します。 メソッドは、クライアントまたはサービス プロバイダーを呼び出すには、警告メッセージを返すことができる場合、は、0 または 0 以外のチェックではなく、戻り値をテストするのには**HR_FAILED**マクロを使用します。 警告、0 以外の値がエラー コード点で異なります、上位ビットの設定はありません。 クライアントまたはサービス プロバイダーが、マクロを使用しない場合に、障害の警告を区別できない場合がありますが可能性があります。 
  
ほとんどのインターフェイスのメソッドと関数は、HRESULT 値を返す、いくつかの関数は、符号なしの long 値を返します。 また、MAPI 環境で使用されるいくつかの方法は、COM から、MAPI エラー値ではなく COM エラー値を返します。 呼び出しを行うときは、次のガイドラインに留意してください。
  
- 依存しないようにするか、 **IUnknown::AddRef**または**が**からの戻り値を使用します。 これらの戻り値は、診断のためだけにします。 
    
- **IUnknown::QueryInterface**は、常に MAPI エラーではなく、FACILITY_NULL または FACILITY_RPC、施設では、汎用の COM エラーを返します。 
    
- 他のすべてのインターフェイス メソッドでは、FACILITY_ITF、または FACILITY_RPC の機能を持つ MAPI インターフェイスのエラーまたは FACILITY_NULL エラーを返します。
    
MAPI のサポートされていないメソッドの呼び出しが行われると、次の 4 つの可能なエラーのいずれかが返されます。 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION。 
  


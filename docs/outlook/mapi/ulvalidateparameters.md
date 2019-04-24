---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315289"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
内部関数を呼び出して、クライアントアプリケーションがサービスプロバイダーと MAPI に渡されたことを確認します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>パラメーター

 _eMethod_
  
> 順番検証するメソッドを列挙で指定します。 
    
 _First_
  
> 順番スタック上の最初の引数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。
    
## <a name="remarks"></a>解説

ulvalidateparameters マクロは[ulvalidateparameters](ulvalidateparms.md)マクロによって置き換えられました。 **** **ulvalidateparameters**は RISC プラットフォームでは正しく動作せず、これでコンパイルができなくなりました。 これは依然としてコンパイルされており、Intel プラットフォームで正常に動作しますが、 **ulvalidateparms**をすべてのプラットフォームで使用することをお勧めします。 
  


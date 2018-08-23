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
ms.openlocfilehash: 297b5a516f8275b236092f9f385afcb673c95de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585242"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
パラメーターのクライアント アプリケーションが、サービス ・ プロバイダーおよび MAPI 経過をチェックする内部関数が呼び出されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapival.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
HRESULT UlValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>パラメーター

 _」方法_
  
> [in]確認する方法を列挙型を指定します。 
    
 _First/先頭のレコード_
  
> [in]スタック上の最初の引数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。
    
## <a name="remarks"></a>注釈

[UlValidateParms](ulvalidateparms.md)マクロでは、 **UlValidateParameters**マクロを置き換えられています。 **UlValidateParameters**は、RISC プラットフォームで正常に動作しないとしてコンパイルができなきます。 それをコンパイルし、インテルのプラットフォームで正常に動作しますが、すべてのプラットフォームで**UlValidateParms**をお勧めします。 
  


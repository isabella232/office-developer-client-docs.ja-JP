---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1a1736001faee62e498784c8a28d24b40f43b781
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624000"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
内部関数を呼び出して、クライアント アプリケーションがサービス プロバイダーと MAPI に渡したパラメーターを確認します。 
  
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
  
> [in]列挙で検証するメソッドを指定します。 
    
 _First_
  
> [in]スタックの最初の引数へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生源のエラーにより、操作が完了しなかっていません。
    
## <a name="remarks"></a>注釈

**UlValidateParameters** マクロは [、UlValidateParms](ulvalidateparms.md)マクロに取ってかえされています。 **UlValidateParameters** は RISC プラットフォームで正しく動作し、コンパイルが行えなくなります。 Intel プラットフォームではコンパイルおよび正常に動作しますが、すべてのプラットフォームで **UlValidateParms** が推奨されます。 
  


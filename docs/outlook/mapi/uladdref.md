---
title: UlAddRef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlAddRef
api_type:
- COM
ms.assetid: 9b897cbc-90b2-4c60-b5f1-dc78e7e7952d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f9e55153830dbe41a2b4a48454157c900d96cf90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315373"
---
# <a name="uladdref"></a>UlAddRef

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
OLE メソッド**IUnknown:: AddRef**を呼び出すための別の方法を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
ULONG UlAddRef(
  LPVOID punk
);
```

## <a name="parameters"></a>パラメーター

 _パンク_
  
> 順番**IUnknown**インターフェイスから派生したインターフェイスへのポインター、つまり任意の MAPI インターフェイス。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しないまたは不明な配信元のエラーにより、操作が完了しませんでした。
    
## <a name="remarks"></a>解説

 **uladdref**は、 **IUnknown:: AddRef**メソッドによって返された値を返します。これは、インターフェイスの参照カウントの新しい値です。 値は0以外の値です。 
  
**iunknown:: AddRef**の詳細については、「 [iunknown インターフェイスを実装する](implementing-the-iunknown-interface.md)」を参照してください。 
  


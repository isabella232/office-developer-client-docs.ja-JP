---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 46c37dbcf1aa3b0469281b8db99f210bda0918be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582302"
---
# <a name="ulrelease"></a>UlRelease

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**** OLE メソッドを呼び出す別の方法を提供します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a>パラメーター

 _パンク_
  
> [in]インターフェイスへのポインターは、任意の MAPI インターフェイスに、 **IUnknown**インターフェイスから派生します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B 
    
MAPI_E_CALL_FAILED 
  
> 予期しない、または不明な発生元のエラーでは、操作を完了できませんでした。
    
## <a name="remarks"></a>注釈

参照カウントは、既存のポインターを解放するオブジェクトの数です。 
  
_Punk_パラメーターが NULL の場合は、**リ ス**を呼び出さずに、関数は直ちに戻ります
  
 **UlRelease**は、リリースするオブジェクトの参照カウントと同じにすることができます**が**メソッドによって返される値を返します。 
  
**リ ス**の詳細については、 [IUnknown インターフェイスを実装する](implementing-the-iunknown-interface.md)を参照してください。 
  


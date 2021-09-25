---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 61da9b3eb173c8d33dfc0d2c29d39f03895f47c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587889"
---
# <a name="iprofadmingetlasterror"></a>IProfAdmin::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル管理オブジェクト [に発生](mapierror.md) した以前のエラーに関する情報を含む MAPIERROR 構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_ パラメーターで返される [MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。 _戻す MAPIERROR 構造体がない場合、lppMAPIError_ パラメーターを **NULL に** 設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

**IProfAdmin::GetLastError** メソッドは、プロファイル管理オブジェクトのメソッド呼び出しから返された最後のエラーに関する情報を取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI が 1 つを提供する場合 **、MAPIERROR** 構造体を使用できます  _。lppMAPIError_ パラメーターが指すのは **、GetLastError** が値を返す場合S_OK。 MAPI では、最後のエラーが何だったのか、またはエラーについて報告する必要がなにもない場合があります。 この状況では  _、lppMAPIError_ で NULL へのポインターが返されます。 
  
**MAPIERROR** 構造体に対して MAPI によって割り当てられたすべてのメモリを解放するには [、MAPIFreeBuffer 関数を呼び出](mapifreebuffer.md)します。 
  
**GetLastError メソッドの詳細については、「Using Extended Errors** [」を参照してください](mapi-extended-errors.md)。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


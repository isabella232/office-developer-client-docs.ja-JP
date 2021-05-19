---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425877"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア オブジェクト [に対して](mapierror.md) 発生した最後のエラーに関する情報を含む MAPIERROR 構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]メッセージ ストア オブジェクトの前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_ パラメーターで返される **MAPIERROR** 構造体の文字列は、Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む、返される **MAPIERROR** 構造体へのポインターへのポインター。 _戻す MAPIERROR がない場合は、lppMAPIError_ パラメーター **を NULL に** 設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

**IMSLogon::GetLastError** メソッドを使用して、メッセージ ストア オブジェクトのメソッド呼び出しから返された最後のエラーに関する情報をユーザーにメッセージで表示します。 
  
返される **MAPIERROR** 構造に対して MAPI によって割り当てられたすべてのメモリを解放するには、クライアント アプリケーションが [MAPIFreeBuffer](mapifreebuffer.md) 関数のみを呼び出す必要があります。 
  
アプリケーションが MAPIERROR を使用するには **、GetLastError** S_OK戻り値を使用する **必要があります**。 戻り値が指定S_OK **MAPIERROR** が返されない場合があります。 実装で最後のエラーが何だったのか判断できない場合、または **MAPIERROR** がエラーに対して使用できない場合 **、GetLastError** は  _代わりに lppMAPIError_ で NULL へのポインターを返します。 
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317298"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアオブジェクトに対して発生した最後のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> 順番以前のメソッド呼び出しでメッセージストアオブジェクトに対して生成されたエラー値を含む HRESULT データ型。
    
 _ulFlags_
  
> 順番返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_パラメーターで返される**MAPIERROR**構造体の文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む、返された**MAPIERROR**構造体へのポインターへのポインター。 返す**MAPIERROR**が存在しない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
## <a name="remarks"></a>解説

**IMSLogon:: GetLastError**メソッドを使用すると、メッセージにメッセージとして表示される情報を取得するために、メッセージストアオブジェクトに対するメソッド呼び出しから返された最後のエラーに関する情報を取得します。 
  
返された**MAPIERROR**構造に対して MAPI によって割り当てられたすべてのメモリを解放するには、クライアントアプリケーションは[MAPIFreeBuffer](mapifreebuffer.md)関数のみを呼び出す必要があります。 
  
アプリケーションが**MAPIERROR**を使用するには、 **GetLastError**の戻り値が S_OK である必要があります。 戻り値が S_OK の場合でも、 **MAPIERROR**は返されない可能性があります。 最後のエラーが発生したかどうかを実装が判断できない場合、またはそのエラーに対して**MAPIERROR**が使用できない場合、 **GetLastError**は_lppMAPIError_で NULL へのポインターを返します。 
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)


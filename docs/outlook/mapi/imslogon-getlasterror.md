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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801067"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**適用されます**: Outlook 
  
メッセージ ストアのオブジェクトに対して発生した最後のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in]メッセージ ストア オブジェクトの以前のメソッドの呼び出しで生成されたエラー値を含む HRESULT のデータ型です。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> _LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する返された**MAPIERROR**構造体へのポインターへのポインター。 返すには、 **MAPIERROR**がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
## <a name="remarks"></a>備考

最後に、メッセージ ストアのオブジェクトのメソッドの呼び出しから返されるエラーに関するユーザーへのメッセージに表示するのに情報を取得するために**IMSLogon::GetLastError**メソッドを使用します。 
  
返された**MAPIERROR**構造体は、MAPI によって割り当てられたすべてのメモリを解放するには、クライアント アプリケーションにのみ、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出す必要があります。 
  
**GetLastError**からの戻り値は、 **MAPIERROR**を使用するアプリケーションの S_OK をする必要があります。 戻り値が S_OK の場合であって、 **MAPIERROR**が返されません。 実装は、最後のエラーが特定できない場合、または、 **MAPIERROR**は、エラー、 **GetLastError**のポインターを返します NULL に_lppMAPIError_の代わりには使用できません。 
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon: IUnknown](imslogoniunknown.md)


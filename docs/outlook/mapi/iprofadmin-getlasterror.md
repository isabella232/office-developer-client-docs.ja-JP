---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430774"
---
# <a name="iprofadmingetlasterror"></a>IProfAdmin::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル管理オブジェクトに発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> 順番前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。
    
 _ulFlags_
  
> 順番返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_パラメーターで返される[MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。 返す**MAPIERROR**構造体がない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
## <a name="remarks"></a>注釈

**IProfAdmin:: GetLastError**メソッドは、プロファイル管理オブジェクトのメソッド呼び出しから返された最後のエラーに関する情報を取得します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MAPIERROR**構造体は、 _lppMAPIError_パラメーターで指定された MAPI が S_OK を返す場合にのみ**** 使用できます。 MAPI では、エラーについてのレポートを作成するために最後のエラーが発生したかどうかを判断できない場合があります。 このような場合、 _lppMAPIError_で NULL へのポインターが返されます。 
  
**MAPIERROR**構造の MAPI に割り当てられているすべてのメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。 
  
**GetLastError**メソッドの詳細については、「[拡張エラーの使用](mapi-extended-errors.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


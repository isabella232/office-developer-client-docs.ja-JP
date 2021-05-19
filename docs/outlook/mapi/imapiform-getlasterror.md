---
title: IMAPIFormGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetLastError
api_type:
- COM
ms.assetid: 81af8a0b-4ec2-459c-8ab2-29d28a8b680f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a74ad733b91aa455b8e03e6aac8efa2c4299b640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426906"
---
# <a name="imapiformgetlasterror"></a>IMAPIForm::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム オブジェクトによって生成された以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。 
  
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
  
> 設定すると _、lppMAPIError_ パラメーターで返される **MAPIERROR** 構造体の文字列は Unicode 形式になります。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む、返される **MAPIERROR** 構造体へのポインターへのポインター。 このパラメーターは、MAPIERROR 構造体を返す **必要** がない場合は NULL に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され **、GetLastError** が Unicode をサポートしていないか、または設定されていない場合MAPI_UNICODE **GetLastError** は Unicode のみをサポートします。 
    
## <a name="remarks"></a>注釈

**IMAPIForm::GetLastError** メソッドは、失敗した以前のメソッド呼び出しに関する情報を提供します。 発信者は **、MAPIERROR** 構造のデータをダイアログ ボックスに含めて、エラーに関する詳細情報をユーザーに提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI が 1 つを提供する場合 _、lppMAPIError_ パラメーターが示す **MAPIERROR** 構造を使用できるのは **、GetLastError** がデータを返す場合S_OK。 MAPI では、最後のエラーが何だったのか判断できない場合や、エラーについて報告する必要がなにもない場合があります。 この状況では、代わりに  _lppMAPIError_ で NULL へのポインターが返されます。 
  
**GetLastError メソッドの詳細については、「Using Extended Errors** [」を参照してください](mapi-extended-errors.md)。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


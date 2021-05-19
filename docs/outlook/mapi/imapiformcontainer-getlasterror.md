---
title: IMAPIFormContainerGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetLastError
api_type:
- COM
ms.assetid: 04952b51-f005-4933-a1d1-695c6dc736cc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e020c66a46f1f195a5731ef1cb3f4b0488162a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415671"
---
# <a name="imapiformcontainergetlasterror"></a>IMAPIFormContainer::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム コンテナー オブジェクトによって生成された以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。 
  
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
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む、返される **MAPIERROR** 構造体へのポインターへのポインター。 _戻す MAPIERROR 構造体がない場合、lppMAPIError_ パラメーターを **NULL に** 設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され **、GetLastError** が Unicode をサポートしていないか、または設定されていない場合MAPI_UNICODE **GetLastError** は Unicode のみをサポートします。 
    
## <a name="remarks"></a>注釈

**IMAPIFormContainer::GetLastError** メソッドは、失敗した以前のメソッド呼び出しに関する情報を提供します。 発信者は **、MAPIERROR** 構造のデータをダイアログ ボックスに含めて、エラーに関する詳細情報をユーザーに提供できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**GETLastError** がデータを返す場合にのみ、MAPI が 1 つを提供する場合は _、lppMAPIError_ パラメーターが指す **MAPIERROR** 構造をS_OK。 MAPI では、最後のエラーが何だったのか判断できない場合や、エラーについて報告する必要がなにもない場合があります。 この状況では、代わりに  _lppMAPIError_ で NULL へのポインターが返されます。 
  
**GetLastError メソッドの詳細については、「Using Extended Errors** [」を参照してください](mapi-extended-errors.md)。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


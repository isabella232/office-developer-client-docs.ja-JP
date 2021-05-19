---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419003"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの前 [のエラー](mapierror.md) に関する情報を含む MAPIERROR 構造体を返します。 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>パラメーター

 _hResult_
  
> [in]前のメソッド呼び出しで生成されたエラーを含む HRESULT。
    
 _ulFlags_
  
> [in]返される文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> _lppMAPIError_ パラメーターで返される **MAPIERROR** 構造体の文字列は、Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppMAPIError_
  
> [out]エラーのバージョン、コンポーネント、コンテキスト情報を含む、返される **MAPIERROR** 構造体へのポインターへのポインター。 _適切な情報を持つ MAPIERROR_ 構造体を指定できない場合は、lppMAPIError パラメーターを **NULL** に設定できます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定MAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

**IMAPITable::GetLastError** メソッドは、エラーが発生した以前のメソッド呼び出しに関する詳細情報 (利用可能な場合) を返します。 この情報は、メッセージまたはダイアログ ボックスに表示できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

ユーザー **にエラーに関** する情報を表示する必要がある場合は常に GetLastError を呼び出します。 
  
テーブル オブジェクトが 1 つを提供する場合は **、GetLastError** が関数を返す場合にのみ _、lppMAPIError_ パラメーターが指す [MAPIERROR](mapierror.md)構造をS_OK。 テーブルの実装では、最後のエラーが何だったのかを判断できない場合や、エラーについて報告する必要がなにもない場合があります。 この状況では  _、lppMAPIError のポインターは_ NULL に設定されます。 
  
**MAPIERROR** 構造体に割り当てられているすべてのメモリを解放するには [、MAPIFreeBuffer 関数を呼び出](mapifreebuffer.md)します。 
  
**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。
  
## <a name="see-also"></a>関連項目



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


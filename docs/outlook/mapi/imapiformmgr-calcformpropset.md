---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436427"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのグループが使用するプロパティの配列を返します。
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>パラメーター

 _pfrminfoarray_
  
> [in]プロパティを返すフォームを識別するフォーム情報オブジェクトの配列へのポインター。
    
 _ulFlags_
  
> [in]  _ppResults_ パラメーターのプロパティ配列がどのように返されるのか制御するフラグのビットマスク。 次のフラグを設定できます。 
    
FORMPROPSET_INTERSECTION 
  
> 返される配列には、フォームのプロパティの交差部分が含まれる。
    
FORMPROPSET_UNION 
  
> 返される配列には、フォームのプロパティの共用体が含まれる。
    
MAPI_UNICODE 
  
> 配列で返される文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _ppResults_
  
> [out]フォームが使用するプロパティを含む [、返される SMAPIFormPropArray](smapiformproparray.md) 構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::CalcFormPropSet** メソッドを呼び出して、フォームのグループが使用するプロパティの配列を取得します。 **CalcFormPropSet** は  _、ulFlags_ パラメーターで設定されたフラグに応じて、これらのフォームのプロパティ セットの交差または共用体を取得し、結果のプロパティ グループを含む **SMAPIFormPropArray** 構造体を返します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォーム ビューアーが  _ulFlags_ パラメーター MAPI_UNICODEフラグを渡す場合、すべての文字列を Unicode 文字列として返す必要があります。 Unicode 文字列をサポートしないフォーム ライブラリ プロバイダーは、渡された場合MAPI_E_BAD_CHARWIDTHをMAPI_UNICODEする必要があります。 
  
## <a name="see-also"></a>関連項目



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


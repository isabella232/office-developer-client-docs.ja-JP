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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342085"
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
  
> 順番プロパティを返すフォームを識別するフォーム情報オブジェクトの配列へのポインター。
    
 _ulFlags_
  
> 順番_ppResults_パラメーターのプロパティ配列を返す方法を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
FORMPROPSET_INTERSECTION 
  
> 返される配列には、フォームのプロパティの共通部分が含まれています。
    
FORMPROPSET_UNION 
  
> 返される配列には、フォームのプロパティの和集合が含まれています。
    
MAPI_UNICODE 
  
> 配列で返される文字列は、Unicode 形式になっています。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _ppResults_
  
> 読み上げ返された[smapiformproparray](smapiformproparray.md)の構造体へのポインターへのポインター。これには、フォームで使用するプロパティが含まれています。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
## <a name="remarks"></a>解説

フォーム閲覧者は、 **imapiformmgr:: CalcFormPropSet**メソッドを呼び出して、フォームのグループが使用するプロパティの配列を取得します。 **CalcFormPropSet**は、 _ulflags_パラメーターで設定されているフラグに応じて、これらのフォームのプロパティセットの積集合または和集合を受け取り、結果として得られるグループを含む**smapiformproparray**の構造を返します。プロパティ. 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームビューアーが_ulflags_パラメーターの MAPI_UNICODE フラグを渡す場合は、すべての文字列が UNICODE 文字列として返されます。 Unicode 文字列をサポートしていないフォームライブラリプロバイダーは、MAPI_UNICODE が渡された場合は MAPI_E_BAD_CHARWIDTH を返します。 
  
## <a name="see-also"></a>関連項目



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


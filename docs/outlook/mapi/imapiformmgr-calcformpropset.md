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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: abd2a3e2a1a810f902ad977413c89f2e8b0113a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800539"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**適用されます**: Outlook 
  
フォームのグループを使用するプロパティの配列を返します。
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parameters

 _pfrminfoarray_
  
> [in]プロパティを返す対象となるフォームを識別するオブジェクトのフォーム情報の配列へのポインター。
    
 _ulFlags_
  
> [in]_PpResults_パラメーターのプロパティの配列を返す方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
FORMPROPSET_INTERSECTION 
  
> 返される配列には、フォームのプロパティの積集合が含まれています。
    
FORMPROPSET_UNION 
  
> 返される配列には、フォームのプロパティの和集合が含まれています。
    
MAPI_UNICODE 
  
> 配列で返される文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _ppResults_
  
> [out]返された[SMAPIFormPropArray](smapiformproparray.md)構造体をフォームを使用するプロパティが含まれているへのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
## <a name="remarks"></a>備考

フォームの閲覧者は、フォームのグループを使用するプロパティの配列を取得する**IMAPIFormMgr::CalcFormPropSet**メソッドを呼び出します。 **CalcFormPropSet**には、交差、または共用体のこれらのフォームのプロパティ セットには、 _ulFlags_パラメーターとその設定のフラグによっての結果として得られるグループを格納する**SMAPIFormPropArray**構造体を返します。プロパティです。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

フォーム ビューアーでは、 _ulFlags_パラメーターに MAPI_UNICODE フラグが成功した場合のすべての文字列が Unicode の文字列として返されます。 Unicode 文字列をサポートしていないフォーム ライブラリ プロバイダーは、MAPI_UNICODE が渡された場合、MAPI_E_BAD_CHARWIDTH を返す必要があります。 
  
## <a name="see-also"></a>関連項目



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)


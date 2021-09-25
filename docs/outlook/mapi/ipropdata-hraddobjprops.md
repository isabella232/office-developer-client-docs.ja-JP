---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b726369dff524feb509bcf9b9728184001da2f7c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561391"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの種類のプロパティを 1 つ以上PT_OBJECTオブジェクトに追加します。
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>パラメーター

 _lpPropTagArray_
  
> [in]追加するプロパティを示すプロパティ タグの配列へのポインター。
    
 _lppProblems_
  
> [in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体または NULL への有効なポインター。 出力時に、追加できないプロパティまたは NULL に関する情報を含む構造体へのポインターを指すポインター。 プロパティの問題配列構造へのポインターは、有効なポインターが渡された場合にのみ返されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常に追加されました。
    
MAPI_E_INVALID_TYPE 
  
> _lpPropTagArray_ パラメーター PT_OBJECT示す配列に渡されたプロパティ以外のプロパティの種類。 
    
MAPI_E_NO_ACCESS 
  
> オブジェクトは、読み取り/書き込みアクセス許可を許可しない設定されています。
    
MAPI_W_PARTIAL_COMPLETION 
  
> プロパティの一部が追加されましたが、すべてではありません。
    
## <a name="remarks"></a>注釈

**IPropData::HrAddObjProps** メソッドは、オブジェクトの種類のプロパティを 1 つ以上PT_OBJECTオブジェクトに追加します。 **HrAddObjProps** は **、SetProps** を呼び出してオブジェクト プロパティを作成できないので、オブジェクト プロパティの [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドの代わりに使用できます。 オブジェクト プロパティを追加すると [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが返すプロパティ タグの一覧にプロパティ タグが含まれます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**HrAddObjProps** が MAPI_W_PARTIAL_COMPLETION を返し _、lppProblems_ を有効なポインターに設定している場合は、返された [SPropProblemArray](spropproblemarray.md)構造体を確認して、追加されていないプロパティを確認します。 通常、発生する唯一の問題はメモリ不足です。 終わったら、MAPIFreeBuffer 関数を呼び出して **SPropProblemArray** 構造体を解放します。 [](mapifreebuffer.md) 
  
プロパティを追加するには、ターゲット オブジェクトに読み取り/書き込みアクセス許可が必要です。 **HrAddObjProps** がオブジェクトをMAPI_E_NO_ACCESS場合は、変更を許可しないので、オブジェクトにプロパティを追加できません。 **HrAddObjProps** を呼び出す前にオブジェクトに対する読み取り/書き込みアクセス許可を取得するには [、IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md)を呼び出し _、ulAccess_ パラメーターを IPROP_READWRITE に設定します。 
  
## <a name="see-also"></a>関連項目



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)


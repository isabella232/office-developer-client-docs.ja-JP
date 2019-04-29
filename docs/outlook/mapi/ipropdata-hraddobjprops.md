---
title: ipropdatahraddobjprops
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416385"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトに PT_OBJECT 型の1つ以上のプロパティを追加します。
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>パラメーター

 _lpPropTagArray_
  
> 順番追加するプロパティを示すプロパティタグの配列へのポインター。
    
 _lppproblems 問題_
  
> [入力]入力時、 [spropの配列](spropproblemarray.md)構造体への有効なポインター、または NULL。 出力時に、追加できなかったプロパティに関する情報を含む構造体へのポインター、または NULL。 プロパティ問題の配列構造体へのポインターは、有効なポインターが渡された場合にのみ返されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロパティが正常に追加されました。
    
MAPI_E_INVALID_TYPE 
  
> PT_OBJECT 以外のプロパティの種類が、 _lpPropTagArray_パラメーターが指す配列に渡されました。 
    
MAPI_E_NO_ACCESS 
  
> オブジェクトには、読み取り/書き込みアクセス許可が設定されていません。
    
MAPI_W_PARTIAL_COMPLETION 
  
> プロパティのいくつかは追加されていますが、全部ではありません。
    
## <a name="remarks"></a>注釈

**ipropdata:: hraddobjprops**メソッドは、オブジェクトに PT_OBJECT 型の1つ以上のプロパティを追加します。 **hraddobjprops**は、オブジェクトプロパティの[imapiprop:: setprops](imapiprop-setprops.md)メソッドに代わる方法を提供します。これは、 **setprops**を呼び出すことでオブジェクトのプロパティを作成できないためです。 [imapiprop:: getproplist](imapiprop-getproplist.md)メソッドによって返される property タグのリストに含まれる property タグに、オブジェクトプロパティの結果が追加されました。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**hraddobjprops**が MAPI_W_PARTIAL_COMPLETION を返し、 _lppproblems 問題_を有効なポインターに設定している場合は、返された[spropprops 配列](spropproblemarray.md)構造を調べて、追加されなかったプロパティを確認します。 通常、発生する問題はメモリが不足していることだけです。 完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 **spropの配列**構造を解放します。 
  
プロパティを追加するには、ターゲットオブジェクトが読み取り/書き込みアクセス許可を持っている必要があります。 **hraddobjprops**が MAPI_E_NO_ACCESS を返す場合は、変更が許可されていないため、オブジェクトにプロパティを追加することはできません。 **hraddobjprops**を呼び出す前に、オブジェクトへの読み取り/書き込みアクセス許可を取得するには、 [ipropdata:: HrSetObjAccess](ipropdata-hrsetobjaccess.md)を呼び出し、 _ulaccess_パラメーターを IPROP_READWRITE に設定します。 
  
## <a name="see-also"></a>関連項目



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)


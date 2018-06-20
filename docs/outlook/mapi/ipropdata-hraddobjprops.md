---
title: IPropDataHrAddObjProps
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 985b763ade9670c064c6c338953debf7beaa2783
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801148"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**適用されます**: Outlook 
  
PT_OBJECT の種類の 1 つまたは複数のプロパティをオブジェクトに追加します。
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>�p�����[�^�[

 _lpPropTagArray_
  
> [in]追加するプロパティを指定するプロパティ タグの配列へのポインター。
    
 _lppProblems_
  
> [で [チェック アウト]入力がある、 [SPropProblemArray](spropproblemarray.md)構造体への有効なポインターまたは NULL。 [出力、追加できませんでしたのプロパティに関する情報を格納する構造体へのポインターへのポインターまたは NULL。 プロパティの問題の配列の構造体へのポインターが有効なポインターが渡された場合にのみ返されます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロパティに追加されました。
    
MAPI_E_INVALID_TYPE 
  
> プロパティは、PT_OBJECT は、 _lpPropTagArray_パラメーターが指す配列に渡された以外を入力します。 
    
MAPI_E_NO_ACCESS 
  
> オブジェクトは、読み取り/書き込み権限を許可しないように設定されています。
    
MAPI_W_PARTIAL_COMPLETION 
  
> すべてではなく、いくつかのプロパティが追加されました。
    
## <a name="remarks"></a>備考

**IPropData::HrAddObjProps**メソッドは、PT_OBJECT の種類の 1 つまたは複数のプロパティをオブジェクトに追加します。 **SetProps**を呼び出すことによってオブジェクトのプロパティを作成することはできませんので、 **HrAddObjProps**は代わりに、オブジェクトのプロパティの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを提供します。 [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドで返されるプロパティ タグのリストに含まれているプロパティ タグでオブジェクトのプロパティの結果を追加します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**HrAddObjProps** MAPI_W_PARTIAL_COMPLETION を取得する_lppProblems_の有効なポインターを設定した場合、どのプロパティが追加されていないことを確認する返された[SPropProblemArray](spropproblemarray.md)構造体を確認してください。 通常、発生する唯一の問題は、メモリ不足です。 操作を終了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって、 **SPropProblemArray**構造体を解放します。 
  
プロパティを追加するには、対象のオブジェクトに読み取り/書き込み権限が必要です。 **HrAddObjProps**では、MAPI_E_NO_ACCESS が返された場合の変更が許可されていないために、オブジェクトにプロパティを追加することはできません。 **HrAddObjProps**を呼び出す前にオブジェクトへの読み取り/書き込み権限を取得するには、 [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md)を呼び出すし、 _ulAccess_パラメーターを IPROP_READWRITE に設定します。 
  
## <a name="see-also"></a>関連項目



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)


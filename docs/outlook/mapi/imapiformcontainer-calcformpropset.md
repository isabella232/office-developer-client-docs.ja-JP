---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e88762457df923b88c22bc21845052f39c2fe051
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571816"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム コンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]  _ppResults_ パラメーターのプロパティ配列がどのように返されるのか制御するフラグのビットマスク。 次のフラグを設定できます。 
    
FORMPROPSET_INTERSECTION 
  
> 返される配列には、フォームのプロパティの交差部分が含まれる。
    
FORMPROPSET_UNION 
  
> 返される配列には、フォームのプロパティの共用体が含まれる。
    
MAPI_UNICODE 
  
> 配列で返される文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _ppResults_
  
> [out]返される [SMAPIFormPropArray](smapiformproparray.md) 構造体へのポインターを指すポインター。 この構造には、インストールされているフォームで使用されるプロパティすべてが含まれる。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは **IMAPIFormContainer::CalcFormPropSet** メソッドを呼び出して、フォーム コンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を取得します。 **IMAPIFormContainer::CalcFormPropSet** は [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) メソッドと同様に動作しますが、特定のコンテナーに登録されているフォームごとに動作します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

Unicode 文字列をサポートしないフォーム ライブラリ プロバイダーは、渡された場合MAPI_E_BAD_CHARWIDTHをMAPI_UNICODEする必要があります。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **IMAPIFormContainer::CalcFormPropSet** は  _、ulFlags_ パラメーターで設定されたフラグに応じて、フォームのプロパティ セットの交差または共用体を取得し、結果のプロパティ グループを含む **SMAPIFormPropArray** 構造体を返します。 
  
クライアントが  _ulFlags_ で MAPI_UNICODEフラグを渡す場合、返される文字列はすべて Unicode です。
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b15dc4e467644c2a0c3856372b550c3b55469f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800520"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**適用対象**: Outlook 
  
フォームのコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]_PpResults_パラメーターのプロパティの配列を返す方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
FORMPROPSET_INTERSECTION 
  
> 返される配列には、フォームのプロパティの積集合が含まれています。
    
FORMPROPSET_UNION 
  
> 返される配列には、フォームのプロパティの和集合が含まれています。
    
MAPI_UNICODE 
  
> 配列で返される文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _ppResults_
  
> [out]返された[SMAPIFormPropArray](smapiformproparray.md)構造体へのポインターへのポインター。 この構造体には、インストールされているフォームで使用されるすべてのプロパティが含まれています。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
## <a name="remarks"></a>注釈

クライアント アプリケーションは、フォームのコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を取得する**IMAPIFormContainer::CalcFormPropSet**メソッドを呼び出します。 **IMAPIFormContainer::CalcFormPropSet**は、特定のコンテナーに登録されているすべてのフォーム上で動作する点を除いて、 [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)メソッドと同様に動作します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

Unicode 文字列をサポートしていないフォーム ライブラリ プロバイダーは、MAPI_UNICODE が渡された場合、MAPI_E_BAD_CHARWIDTH を返す必要があります。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **IMAPIFormContainer::CalcFormPropSet**交差または_ulFlags_パラメーターに設定したフラグに応じて、フォームのプロパティのセットの和集合のいずれかは、含まれている**SMAPIFormPropArray**構造体が返されます、プロパティのグループを結果として得られる。 
  
_UlFlags_で、クライアントが、MAPI_UNICODE フラグを渡すと、すべての関数が返す文字列は Unicode です。
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


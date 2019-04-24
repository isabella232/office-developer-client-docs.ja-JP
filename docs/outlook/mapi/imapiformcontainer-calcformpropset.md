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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286588"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を返します。
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番_ppResults_パラメーターのプロパティ配列を返す方法を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
FORMPROPSET_INTERSECTION 
  
> 返される配列には、フォームのプロパティの共通部分が含まれています。
    
FORMPROPSET_UNION 
  
> 返される配列には、フォームのプロパティの和集合が含まれています。
    
MAPI_UNICODE 
  
> 配列で返される文字列は、Unicode 形式になっています。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _ppResults_
  
> 読み上げ返された[smapiformproparray](smapiformproparray.md)の構造体へのポインターへのポインター。 この構造体には、インストールされているフォームで使用されるすべてのプロパティが含まれます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
## <a name="remarks"></a>解説

クライアントアプリケーションは、 **imapiformcontainer:: CalcFormPropSet**メソッドを呼び出して、フォームコンテナーにインストールされているすべてのフォームで使用されるプロパティの配列を取得します。 **imapiformcontainer:: CalcFormPropSet**は、 [imapiformcontainer:: CalcFormPropSet](imapiformmgr-calcformpropset.md)メソッドに似ていますが、特定のコンテナーに登録されているすべてのフォーム上で動作する点が異なります。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

Unicode 文字列をサポートしていないフォームライブラリプロバイダーは、MAPI_UNICODE が渡された場合は MAPI_E_BAD_CHARWIDTH を返します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **imapiformcontainer:: CalcFormPropSet**は、 _ulflags_パラメーターで設定されているフラグに応じて、フォームのプロパティセットの積集合またはユニオンを取得します。この構造体は、次の式を含む**smapiformproparray**結果のプロパティグループ。 
  
クライアントが_ulflags_に MAPI_UNICODE フラグを渡すと、返されるすべての文字列は UNICODE になります。
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


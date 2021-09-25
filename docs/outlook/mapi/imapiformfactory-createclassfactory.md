---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 69b371f5fda78159ff3626148cbc6ef32370a263
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551353"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームのクラス ファクトリ オブジェクトを返します。
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>パラメーター

 _clsidForm_
  
> [in]クラス ファクトリによって作成されるフォームのクラス識別子。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lppClassFactory_
  
> [out]クラス ファクトリ オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> クラス ファクトリ オブジェクトが返されました。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormFactory::CreateClassFactory** メソッドを呼び出して、特定のフォームのクラス ファクトリを取得します。 クラス ファクトリは、特定のクラスのメッセージを処理するフォームのインスタンスを作成し、これらのインスタンスへのアクセスを制御するために使用されます。 
  
**CreateClassFactory メソッド** は、フォーム ビューアーによって呼び出され、複数のメッセージ クラスを実装するフォーム サーバーのクラス ファクトリ オブジェクトを取得します。 このメソッドは、クラス識別子 (CLSID) をパラメーターとして受け取ります。 このパラメーターに基づいて、このメソッドは、返すクラス ファクトリ オブジェクトの特定の種類を決定できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**CreateClassFactory** 実装から、同じクラス識別子に対する複数の呼び出しで同じクラス ファクトリ オブジェクトを返します。 新しいクラス ファクトリ インスタンスを作成する必要はありません。 
  
必要に応じて適切なクラス ファクトリ インスタンスを作成する 1 つのクラス ファクトリ実装、またはメッセージ クラスごとに 1 つの複数のクラス ファクトリ実装を使用できます。
  
## <a name="see-also"></a>関連項目



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)


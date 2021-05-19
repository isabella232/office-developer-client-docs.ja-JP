---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416077"
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


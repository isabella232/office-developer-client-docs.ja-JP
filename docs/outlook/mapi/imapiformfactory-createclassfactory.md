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
  
フォームのクラスファクトリオブジェクトを返します。
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a>パラメーター

 _clsidform_
  
> 順番クラスファクトリによって作成されるフォームのクラス識別子。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lppclassfactory_
  
> 読み上げクラスファクトリオブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> クラスファクトリオブジェクトが返されました。
    
## <a name="remarks"></a>注釈

フォーム閲覧者は、 **imapiformfactory:: CreateClassFactory**メソッドを呼び出して、特定のフォームのクラスファクトリを取得します。 クラスファクトリは、特定のクラスのメッセージを処理するフォームのインスタンスを作成し、それらのインスタンスへのアクセスを制御するために使用されます。 
  
**CreateClassFactory**メソッドは、フォームビューアーによって呼び出され、複数のメッセージクラスを実装するフォームサーバーのクラスファクトリオブジェクトを取得します。 このメソッドは、クラス識別子 (CLSID) をパラメーターとして受け取ります。 このパラメーターに基づいて、このメソッドは、返される特定の種類のクラスファクトリオブジェクトを決定できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

同じクラス識別子に対する複数の呼び出しで、 **CreateClassFactory**実装から同じクラスファクトリオブジェクトを返すことができます。 新しいクラスファクトリインスタンスを作成する必要はありません。 
  
必要に応じて適切なクラスファクトリインスタンスを作成するか、メッセージクラスごとに1つずつ、複数のクラスファクトリの実装を作成する、単一のクラスファクトリ実装を使用できます。
  
## <a name="see-also"></a>関連項目



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)


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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 823e10a1f496f5f5e8bab00f94d700d06e753b48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800547"
---
# <a name="imapiformfactorycreateclassfactory"></a>IMAPIFormFactory::CreateClassFactory

  
  
**適用対象**: Outlook 
  
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
  
> [in]クラス ファクトリによって作成されるフォームのクラス識別子です。
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _lppClassFactory_
  
> [out]クラス ファクトリ オブジェクトへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> クラス ファクトリ オブジェクトが返されました。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは、特定のフォームのクラス ファクトリを取得する**IMAPIFormFactory::CreateClassFactory**メソッドを呼び出します。 クラス ファクトリは、特定のクラスのメッセージを処理するフォームのインスタンスを作成して、これらのインスタンスへのアクセスを制御するために使用されます。 
  
**CreateClassFactory**メソッドは、複数のメッセージ クラスを実装しているフォームのサーバーのクラス ファクトリ オブジェクトを取得するフォーム ビューアーによって呼び出されます。 このメソッドは、クラス識別子 (CLSID) をパラメーターとして受け取ります。 そのパラメーターに基づいて、このメソッドは、返されるクラス ファクトリ オブジェクトの特定の種類を決定できます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

オブジェクトを取得できます、 **CreateClassFactory**の実装から、同じクラス工場出荷時に同じ識別子がクラスの複数の呼び出し。 クラス ファクトリの新しいインスタンスを作成する必要はありません。 
  
1 つのクラス ファクトリの実装を必要に応じて、適切なクラス ファクトリのインスタンスを作成するか、複数のクラス ファクトリ実装は、各メッセージ クラスの 1 つを持つことができます。
  
## <a name="see-also"></a>関連項目



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)


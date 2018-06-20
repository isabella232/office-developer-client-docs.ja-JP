---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c33fea8a2aba875fcdc06dea3343add4b7ac5dde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800522"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**適用されます**: Outlook 
  
開いているフォームのサーバーは、メモリ内に保持します。
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _fLockServer_
  
> [in]の**場合は true**ロック カウントをインクリメントするのにはそれ以外の場合、 **false を指定**します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

フォーム ビューアーは、開いているフォームのサーバー アプリケーションをメモリに保持する**IMAPIFormFactory::LockServer**メソッドを呼び出します。 フォーム サーバーをメモリに保持では、頻繁にフォームが作成され、リリースされたときに、パフォーマンスが向上します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**IMAPIFormFactory::LockServer**メソッドでは、 [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx)メソッドによく似ています。 本質的に、 **IMAPIFormFactory::LockServer**メソッドを維持何度の数が呼び出されました。そのカウントが 0 より大きい場合に限り、メソッドは、メモリからアンロードされるフォームのサーバーを防ぎます。 [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx)関数を使用すると、この機能を実装します。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormFactory: IUnknown](imapiformfactoryiunknown.md)


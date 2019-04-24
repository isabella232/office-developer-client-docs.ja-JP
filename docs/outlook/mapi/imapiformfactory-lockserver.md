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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342141"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
開いているフォームサーバーをメモリに保持します。
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _flockserver_
  
> 順番ロックカウントを増分する場合は true、それ以外の**場合は true** 。それ以外の場合は**false**。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

フォームビューアーは、open form サーバーアプリケーションをメモリに保持する**imapiformfactory:: lockserver**メソッドを呼び出します。 フォームサーバーをメモリに保持すると、フォームが頻繁に作成およびリリースされるときのパフォーマンスが向上します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**imapiformfactory:: lockserver**メソッドは、 [IClassFactory:: lockserver](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx)メソッドによく似ています。 基本的に、 **imapiformfactory:: lockserver**メソッドは、呼び出し回数のカウントを保持します。このカウントが0より大きい限り、このメソッドは、フォームサーバーがメモリからアンロードされないようにします。 [colockobjectexternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx)関数を使用して、これを実装できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)


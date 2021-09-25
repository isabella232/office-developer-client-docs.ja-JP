---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d5aa2068b461a5bba1055ef990a5aff38b113879
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551325"
---
# <a name="imapiformfactorylockserver"></a>IMAPIFormFactory::LockServer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
開いているフォーム サーバーをメモリに保持します。
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _fLockServer_
  
> [in] **ロック数** を増やす場合は true。それ以外の場合は **false です**。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormFactory::LockServer** メソッドを呼び出して、開いているフォーム サーバー アプリケーションをメモリに保持します。 フォーム サーバーをメモリに保持すると、フォームが頻繁に作成およびリリースされる場合のパフォーマンスが向上します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**IMAPIFormFactory::LockServer** メソッドは [、IClassFactory::LockServer メソッドと非常に似](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx)ています。 基本的に **、IMAPIFormFactory::LockServer** メソッドは、呼び出された回数のカウントを保持します。この数が 0 より大きい限り、フォーム サーバーはメモリからアンロードされません。 これを実装するには [、CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) 関数を使用できます。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormFactory : IUnknown](imapiformfactoryiunknown.md)


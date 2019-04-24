---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316588"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
stream にアクセスするためのストレージオブジェクトを実装します。
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>パラメーター

 _lpUnkIn_
  
> 順番stream オブジェクトへのポインターを示します。
    
 _lpinterface_
  
> 順番_lpUnkIn_によって参照されるストリームへのアクセスに使用されるインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 次のいずれかの値が有効です: IID_IStream、IID_ILockBytes、または**null**。これは、このストリームにアクセスするために[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスを使用する必要があることを示します。 
    
 _ulFlags_
  
> 順番stream オブジェクトを基準にして、ストレージオブジェクトを作成する方法を制御するフラグのビットマスク。 既定では、記憶域は読み取り専用アクセスで作成され、ストリームの位置0から開始します。 次のフラグを設定できます。
    
STGSTRM_CREATE 
  
> stream オブジェクト用に新しいストレージオブジェクトを作成する必要があります。
    
STGSTRM_CURRENT 
  
> ストレージオブジェクトは、ストリームの現在の位置から開始する必要があります。
    
STGSTRM_MODIFY 
  
> 呼び出し元は、返されたストレージオブジェクトに対する読み取り/書き込みアクセス許可を持っている必要があります。
    
STGSTRM_RESET 
  
> ストレージオブジェクトは、位置0から開始する必要があります。
    
 _lppstorageout_
  
> 読み上げストレージオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ストレージオブジェクトが正常に作成されました。
    
## <a name="remarks"></a>解説

**imapisupport:: istoragefromstream**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。 サービスプロバイダーは、 **istoragefromstream**を呼び出して、特定のプロパティを開くために使用するストレージオブジェクトを作成します。 [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)インターフェイスを独自に実装しているサービスプロバイダーは、 **istoragefromstream**を呼び出す必要はありません。 
  
**istoragefromstream**によって作成されたストレージオブジェクトは、ストリームの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、参照カウントをインクリメントし、ストレージが解放されたときにカウントをデクリメントします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

いずれかのオブジェクトの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドが呼び出されたときに、 **IStorage**インターフェイスを持つプロパティを開くには、次のタスクを実行します。 
  
1. プロパティの読み取り/書き込み権限を持つ stream オブジェクトを開きます。
    
2. プロパティストリームをストレージオブジェクトとして内部的にマークします。
    
3. ストレージオブジェクトを生成するには、 **istoragefromstream**を呼び出します。 
    
4. このストレージオブジェクトへのポインターを返します。
    
ストレージオブジェクトを使用する追加のインターフェイスを実装する場合は、ストレージオブジェクトをラップするオブジェクトを作成し、より高いレベルの[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドを実装します。 
  
プロパティが**IStorage**を使用して作成された場合、 **IStream**インターフェイスで開くことを許可しません。 反対に、 **IStream**を使用して作成された場合、 **IStorage**インターフェイスでプロパティを開かないようにします。 
  
1つの例外を除き、 **IStreamDocfile**インターフェイスを使用して、あるコンテナーから別のコンテナーに格納オブジェクトをストリームすることはできますが、 **openproperty**メソッドの lpinterface で IID_IStreamDocfile インターフェイス識別子を渡す必要があります。 __ パラメーター。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


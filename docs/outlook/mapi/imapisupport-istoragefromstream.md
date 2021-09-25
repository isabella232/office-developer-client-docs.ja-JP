---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 04cce495a0149b77429467eb814c5b7a6960dd2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575849"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストリームにアクセスするストレージ オブジェクトを実装します。
  
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
  
> [in]ストリーム オブジェクトへのポインター。
    
 _lpInterface_
  
> [in]  _lpUnkIn_ が指すストリームにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 次の値は有効です:IID_IStream、IID_ILockBytes、または **null** は [、IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) インターフェイスを使用してストリームにアクセスする必要があります。 
    
 _ulFlags_
  
> [in]ストリーム オブジェクトを基準にストレージ オブジェクトを作成する方法を制御するフラグのビットマスク。 既定では、ストレージは読み取り専用アクセスで作成され、ストリームは記憶域の位置 0 から始まります。 次のフラグを設定できます。
    
STGSTRM_CREATE 
  
> ストリーム オブジェクト用に新しいストレージ オブジェクトを作成する必要があります。
    
STGSTRM_CURRENT 
  
> 記憶域オブジェクトは、ストリームの現在の位置から開始する必要があります。
    
STGSTRM_MODIFY 
  
> 呼び出し元は、返されるストレージ オブジェクトに対する読み取り/書き込みアクセス許可を持っている必要があります。
    
STGSTRM_RESET 
  
> 記憶域オブジェクトは、位置 0 から始まる必要があります。
    
 _lppStorageOut_
  
> [out]記憶域オブジェクトへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 記憶域オブジェクトが正常に作成されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::IStorageFromStream** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。 サービス プロバイダーは **、IStorageFromStream** を呼び出して、特定のプロパティを開く際に使用するストレージ オブジェクトを作成します。 [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)インターフェイスの独自の実装を持つサービス プロバイダーは **、IStorageFromStream を呼び出す必要があります**。 
  
**IStorageFromStream** によって作成されたストレージ オブジェクトは、ストリームの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、その参照カウントをインクリメントし、ストレージが解放されるとカウントをデクリメントします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

オブジェクトの [1 つの IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドが呼び出され **、IStorage** インターフェイスでプロパティを開く場合は、次のタスクを実行します。 
  
1. プロパティの読み取り/書き込みアクセス許可を持つストリーム オブジェクトを開きます。
    
2. プロパティ ストリームを内部的にストレージ オブジェクトとしてマークします。
    
3. **IStorageFromStream を呼び出して**、ストレージ オブジェクトを生成します。 
    
4. このストレージ オブジェクトへのポインターを返します。
    
ストレージ オブジェクトを使用する追加のインターフェイスを実装する場合は、ストレージ オブジェクトをラップするオブジェクトを作成し、より高い [レベルの IUnknown::QueryInterface メソッドを実装](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) します。 
  
IStorage を使用して作成された **場合は、IStream** インターフェイスでプロパティ **を開かれません**。 逆に、IStream を使用して作成した **場合は、IStorage** インターフェイスでプロパティを **開かれません**。 
  
1 つの例外を除き **、IStreamDocfile** インターフェイスを使用してコンテナー間でストレージ オブジェクトをストリームすることもできますが、IID_IStreamDocfile インターフェイス識別子は **OpenProperty** メソッドの  _lpInterface_ パラメーターで渡す必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


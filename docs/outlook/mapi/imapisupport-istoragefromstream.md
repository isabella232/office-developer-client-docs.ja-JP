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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f1c27f87cb113ebe30a42211035f6f50475a1be3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588182"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ストリームにアクセスするためのストレージ オブジェクトを実装します。
  
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
  
> [in]_LpUnkIn_で指定されたストリームにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 次の値のいずれかが無効です: IID_IStream、IID_ILockBytes、または**null**ストリームにアクセスするのには、 [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスを使用することを示します。 
    
 _ulFlags_
  
> [in]記憶域オブジェクトのストリーム オブジェクトを作成する方法を制御するフラグのビットマスクです。 既定では、読み取り専用アクセス権を持つストレージを作成し、ストリームは、ストレージ内の位置 0 から始まりです。 次のフラグを設定することができます。
    
STGSTRM_CREATE 
  
> 新しいストレージ オブジェクトは、ストリーム オブジェクトを作成してください。
    
STGSTRM_CURRENT 
  
> ストレージ オブジェクト、ストリームの現在位置で開始します。
    
STGSTRM_MODIFY 
  
> 呼び出し元に返された記憶域オブジェクトの読み取り/書き込み権限が必要です。
    
STGSTRM_RESET 
  
> ストレージ オブジェクトは、位置 0 で開始します。
    
 _lppStorageOut_
  
> [out]ストレージ オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ストレージ オブジェクトは正しく作成されました。
    
## <a name="remarks"></a>注釈

サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::IStorageFromStream**メソッドを実装します。 サービス プロバイダーは、特定のプロパティを開くときに使用するストレージ オブジェクトを作成するのには**IStorageFromStream**を呼び出します。 [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx)インターフェイスの独自の実装を持つサービス ・ プロバイダーは、 **IStorageFromStream**を呼び出す必要はありません。 
  
**IStorageFromStream**によって作成されたストレージ オブジェクトは、ストレージが解放されるときにストリームの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)のメソッドの参照カウントと、デクリメントをインクリメントするにカウントを呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**IStorage**インターフェイスを使用してプロパティを開き、オブジェクトの 1 つの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドが呼び出されると、次のタスクを実行します。 
  
1. プロパティの読み取り/書き込み権限を持つ stream オブジェクトを開きます。
    
2. プロパティ ストリームをストレージ オブジェクトとして内部的にマークします。
    
3. ストレージ ・ オブジェクトを生成するのには**IStorageFromStream**を呼び出します。 
    
4. このストレージ オブジェクトへのポインターを返します。
    
ストレージ オブジェクトを使用する追加のインターフェイスを実装する場合、ストレージ オブジェクトをラップするオブジェクトを作成しより高いレベルの[IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)メソッドを実装します。 
  
**IStorage**で作成された場合は、 **IStream**インターフェイスを使用して開かれるプロパティを許可しません。 逆に、 **IStorage**インターフェイスを使用して開く**IStream**で作成されたプロパティを許可しません。 
  
1 つの例外を除き、 **IStreamDocfile**インターフェイスを使用して、1 つのコンテナーから別のストレージ オブジェクトをストリーム配信してもかまいませんが、メソッドでは、 **OpenProperty**の _、IID_IStreamDocfile のインタ フェース識別子を渡す必要があります lpInterface_パラメーター。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


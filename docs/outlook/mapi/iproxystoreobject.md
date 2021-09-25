---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3dad9c850c4564fd1af206df23dc3cd621ea60ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596030"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
インターネット メッセージ アクセス プロトコル (IMAP) ストア オブジェクトを提供します。このオブジェクトを使用すると、同期を呼び出してアイテムをダウンロードすることなく、個人用フォルダー ファイル (PST) 内のアイテムにアクセスできます。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|提供者:  <br/> |メッセージ ストア プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |ラップされていない IMAP ストアへのポインターを取得します。  <br/> |
| *プレースホルダー メンバー*  <br/> | *サポートされていないか、文書化されていません。*  <br/> |
   
## <a name="remarks"></a>注釈

IProxyStoreObject インターフェイスを取得するには、ソース メッセージ ストアで **IUnknown::QueryInterface を呼び出** します。 [](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) 次に **、IProxyStoreObject::UnwrapNoRef** を呼び出して、ラップされていないストア オブジェクトを取得します。 **QueryInterface がエラー** メッセージを返 **MAPI_E_INTERFACE_NOT_SUPPORTED、** ストアはラップされません。 
  
**UnwrapNoRef** はアンラップされたストア オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないので **、UnwrapNoRef** を正常に呼び出した後、参照カウントを維持するために [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。 
  


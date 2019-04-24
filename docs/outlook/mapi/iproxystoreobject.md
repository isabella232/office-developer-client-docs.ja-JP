---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315520"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップが解除され、同期を呼び出してアイテムをダウンロードすることなく個人用フォルダーファイル (PST) 内のアイテムにアクセスできるようにする、インターネットメッセージアクセスプロトコル (IMAP) ストアオブジェクトを提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承元:  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|提供元:  <br/> |メッセージストアプロバイダー  <br/> |
|インターフェイス識別子:  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |ラップされていない IMAP ストアへのポインターを取得します。  <br/> |
| *Placeholder メンバー*  <br/> | *サポートされていないか文書化されていません。*  <br/> |
   
## <a name="remarks"></a>解説

**iproxystoreobject**インターフェイスを取得するには、ソースメッセージストアで[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出します。 その後、 **iproxystoreobject:: UnwrapNoRef**を呼び出して、ラップ解除された store オブジェクトを取得します。 **QueryInterface**がエラー **MAPI_E_INTERFACE_NOT_SUPPORTED**を返した場合、ストアはラップされていません。 
  
**UnwrapNoRef**は、ラップされていない store オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないため、 **UnwrapNoRef**の呼び出しに成功した後で、 [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出して参照カウントを維持する必要があります。 
  


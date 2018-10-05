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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395309"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ラップするがされたため、同期を呼び出すと、アイテムをダウンロードしなくても、個人用フォルダー ファイル (PST) 内のアイテムへのアクセスを許可するインターネット メッセージ アクセス プロトコル (IMAP) ストア オブジェクトを提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承されます。  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|によって提供されます。  <br/> |メッセージ ストア プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |ラップ解除済みの IMAP ストアへのポインターを取得します。  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
   
## <a name="remarks"></a>備考

**IProxyStoreObject**インターフェイスを取得するのには元のメッセージ ストアには、 [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)を呼び出します。 ラップ解除済みストア オブジェクトを取得する**IProxyStoreObject::UnwrapNoRef**を呼び出します。 **QueryInterface**には、エラー **MAPI_E_INTERFACE_NOT_SUPPORTED**が返された場合、ストアがされてラップされません。 
  
**UnwrapNoRef**では、 **UnwrapNoRef**の呼び出しに成功した後はこの新しいオブジェクトへのポインター、ラップが解除されたストアでの参照カウントは増分されません、ために、参照カウントを維持するために[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。 
  


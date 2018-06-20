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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f6566f567c228b6416a64dbd58653561bb592e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801171"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**適用されます**: Outlook 
  
ラップするがされたため、同期を呼び出すと、アイテムをダウンロードしなくても、個人用フォルダー ファイル (PST) 内のアイテムへのアクセスを許可するインターネット メッセージ アクセス プロトコル (IMAP) ストア オブジェクトを提供します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|継承されます。  <br/> |[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) <br/> |
|によって提供されます。  <br/> |メッセージ ストア プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |ラップ解除済みの IMAP ストアへのポインターを取得します。  <br/> |
| *プレース ホルダー メンバー*  <br/> | *いないサポートまたは文書化されています。*  <br/> |
   
## <a name="remarks"></a>備考

**IProxyStoreObject**インターフェイスを取得するのには元のメッセージ ストアには、 [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)を呼び出します。 ラップ解除済みストア オブジェクトを取得する**IProxyStoreObject::UnwrapNoRef**を呼び出します。 **QueryInterface**には、エラー **MAPI_E_INTERFACE_NOT_SUPPORTED**が返された場合、ストアがされてラップされません。 
  
**UnwrapNoRef**では、 **UnwrapNoRef**の呼び出しに成功した後はこの新しいオブジェクトへのポインター、ラップが解除されたストアでの参照カウントは増分されません、ために、参照カウントを維持するために[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。 
  


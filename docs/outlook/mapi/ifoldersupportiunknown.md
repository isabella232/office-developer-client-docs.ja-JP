---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 279f8cf93a42cc886dbabbec7fbe94ac59e31593
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600977"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの共有のサポートに関する情報を提供します。
  
|||
|:-----|:-----|
|提供元:  <br/> |メッセージ ストア プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |フォルダーの共有のサポートに関する情報を取得します。  <br/> |
   
## <a name="remarks"></a>注釈

通常、Microsoft Office Outlookを共有する場合は、MAPI ストア プロバイダーがこのインターフェイスを実装する必要があります。 例外は、このExchange Server実装せずにフォルダーを共有できるストア プロバイダーの例外です。
  
クライアントは **[、IFolderSupport の IMAPIFolder](imapifolderimapicontainer.md)** **を照会できます**。 これが成功した場合は **、IFolderSupport::GetSupportMask** を呼び出し、FS_SUPPORTS_SHARING **を確認** します。 
  


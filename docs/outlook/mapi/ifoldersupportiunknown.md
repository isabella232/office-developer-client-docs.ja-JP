---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a4a1c78e65d9a515b2b42d7e0a2bc3a8b4bd8869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800466"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport: IUnknown

  
  
**適用されます**: Outlook 
  
共有フォルダーのサポートに関する情報を提供します。
  
|||
|:-----|:-----|
|提供元:  <br/> |メッセージ ストア プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |共有フォルダーのサポートに関する情報を取得します。  <br/> |
   
## <a name="remarks"></a>備考

一般に、Microsoft Office Outlook は MAPI プロバイダーは、フォルダーを共有する必要がある場合は、このインターフェイスを実装するプロバイダーを格納する必要があります。 例外は、Exchange Server のストア プロバイダーでこのインターフェイスを実装しなくてもフォルダーを共有することができます。
  
クライアントは、 **IFolderSupport** **[IMAPIFolder](imapifolderimapicontainer.md)** を照会できます。 成功した場合、 **IFolderSupport::GetSupportMask**を呼び出すし、 **FS_SUPPORTS_SHARING**ビットが設定されるを確認します。 
  


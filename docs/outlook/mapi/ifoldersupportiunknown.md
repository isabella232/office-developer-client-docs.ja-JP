---
title: ifoldersupport IUnknown
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415776"
---
# <a name="ifoldersupport--iunknown"></a>IFolderSupport : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの共有のサポートに関する情報を提供します。
  
|||
|:-----|:-----|
|提供元:  <br/> |メッセージストアプロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IFolderSupport  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|**[GetSupportMask](ifoldersupport-getsupportmask.md)** <br/> |フォルダーの共有のサポートに関する情報を取得します。  <br/> |
   
## <a name="remarks"></a>注釈

通常、プロバイダーがフォルダーを共有する場合、Microsoft Office Outlook では、このインターフェイスを実装するために MAPI ストアプロバイダーが必要です。 例外は、このインターフェイスを実装せずにフォルダーを共有できる Exchange サーバーストアプロバイダーです。
  
クライアントは、 **ifoldersupport**の**[imapifolder](imapifolderimapicontainer.md)** に対してクエリを実行できます。 成功した場合は、 **ifoldersupport:: getsupportmask**を呼び出し、 **FS_SUPPORTS_SHARING**ビットが設定されているかどうかを確認します。 
  


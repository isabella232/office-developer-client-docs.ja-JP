---
title: '[よく使うアドレス] ダイアログ ボックスの表示'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a7b603504956be9ec3066e5ff5e1d5db7d59852a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799961"
---
# <a name="displaying-the-common-address-dialog-box"></a>[よく使うアドレス] ダイアログ ボックスの表示

  
  
**適用対象**: Outlook 
  
MAPI の [アドレス] コモン ダイアログ ボックスは、さまざまな受信者リストを構築するなどのアドレス指定のタスクを使用できます。 このダイアログ ボックスを表示するには、 **IAddrBook::Address**を呼び出します。 多くのパラメーターを設定して、それらの組み合わせによって、特定のコンテナーから、特定の種類のエントリを表示を制限できます。
  
 **個人用アドレス帳 (PAB) のエントリのみを表示するのには、[アドレス] ダイアログ ボックスを制限するには**
  
1. 個人アドレス帳のエントリ id を取得するために[られたユーザーのプライマリ](iaddrbook-getpab.md)を呼び出します。 
    
2. として RELOP_EQ を使用して、 **relop** 、 [SPropertyRestriction](spropertyrestriction.md)の構造と、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) または**PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) のメンバーのプロパティ制約を作成します**ulPropTag**のメンバーです。 **PR_ENTRYID**を使用する場合は、 **GetPAB**から取得したエントリの識別子を渡します。 **PR_AB_PROVIDER_ID**を使用する場合は、MSPAB に含まれている値を渡します。H ヘッダー ファイルです。 **PR_AB_PROVIDER_ID**は、MAPI によって設計された PAB の一意の識別子です。 
    
3. プロパティ制限を指定する_lpHierRestriction_パラメーターで[IAddrBook::Address](iaddrbook-address.md)を呼び出します。 
    


---
title: '[共通アドレス] ダイアログボックスを表示する'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337094"
---
# <a name="displaying-the-common-address-dialog-box"></a>[共通アドレス] ダイアログボックスを表示する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPI 共通アドレス] ダイアログボックスは、受信者リストの作成など、さまざまなアドレス指定タスクに使用できます。 このダイアログボックスを表示するには、 **IAddrBook:: Address**を呼び出します。 設定されているパラメーターの種類およびそれらの設定方法に応じて、特定のコンテナーから特定の種類のエントリへの表示を制限することができます。
  
 **[アドレス] ダイアログボックスで個人用アドレス帳 (PAB) エントリのみを表示するように制限するには**
  
1. [IAddrBook:: getpab](iaddrbook-getpab.md)を呼び出して、pab のエントリ識別子を取得します。 
    
2. [spropertyrestriction](spropertyrestriction.md)構造の**relop**メンバに対して RELOP_EQ を使用し、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) または**PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) のどちらかとしてのプロパティ制限を作成します。**ulPropTag**メンバー。 **PR_ENTRYID**を使用する場合は、 **getpab**から取得したエントリ識別子を渡します。 **PR_AB_PROVIDER_ID**を使用する場合は、mspab に含まれる値を渡します。H ヘッダーファイル。 **PR_AB_PROVIDER_ID**は、MAPI によって設計された PAB の一意の識別子です。 
    
3. プロパティ制限を指す_lpHierRestriction_パラメーターを使用して、 [IAddrBook:: Address](iaddrbook-address.md)を呼び出します。 
    


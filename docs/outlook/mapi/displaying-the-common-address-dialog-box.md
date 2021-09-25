---
title: '[共通アドレス] ダイアログ ボックスの表示'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 81264e5cbf84bf4b8dcbed6ab31c7909fa04483d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596576"
---
# <a name="displaying-the-common-address-dialog-box"></a>[共通アドレス] ダイアログ ボックスの表示

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPI 共通アドレス] ダイアログ ボックスは、受信者リストの作成など、さまざまなアドレス指定タスクに使用できます。 このダイアログ ボックスを表示するには **、IAddrBook::Address を呼び出します**。 設定する多くのパラメーターの種類と設定方法に応じて、特定のコンテナーの特定の種類のエントリに表示を制限できます。
  
 **[アドレス] ダイアログ ボックスに個人用アドレス帳 (PAB) エントリのみを表示するには**
  
1. [IAddrBook::GetPAB](iaddrbook-getpab.md)を呼び出して、PAB のエントリ識別子を取得します。 
    
2. [SPropertyRestriction](spropertyrestriction.md)構造体の relop メンバーに RELOP_EQを使用し **、ulPropTag** メンバーとして PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) または **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) を使用するプロパティ制限を作成します。  このプロパティを **使用PR_ENTRYID** GetPAB から取得したエントリ識別子 **を渡します**。 この値を使用 **PR_AB_PROVIDER_ID** MSPAB に含まれる値を渡します。H ヘッダー ファイル。 **PR_AB_PROVIDER_ID** は、MAPI によって設計された PAB の一意の識別子です。 
    
3. プロパティ制限を指す _lpHierRestriction_ パラメーターを使用して [IAddrBook::Address](iaddrbook-address.md)を呼び出します。 
    


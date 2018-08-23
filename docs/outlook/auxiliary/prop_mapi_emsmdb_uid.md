---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Exchange アカウントの UID を含む ACCT_BIN 構造体を表します。
ms.openlocfilehash: 05e2e61601a08e0cb6f6dc99d265f12a10b19d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799588"
---
# <a name="propmapiemsmdbuid"></a>PROP_MAPI_EMSMDB_UID

Exchange アカウントの UID を含む[ACCT_BIN](acct_bin.md)構造体を表します。 
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x2009  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ。  <br/> |0x20090102  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。
  
[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)を使用して、アカウントが Exchange アカウントかどうかを確認します。 場合は、**プロペラ\_MAPI_EMSMDB_UID** 、 **emsmdbUID**は、Exchange アカウントの一意の ID が含まれています**ACCT_BIN**は、です。 アカウントが Exchange アカウントでない場合は、このプロパティは定義されていません。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [複数の Exchange アカウントの使用](http://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [PidTagExchangeProfileSectionId ���K���̃v���p�e�B](http://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)


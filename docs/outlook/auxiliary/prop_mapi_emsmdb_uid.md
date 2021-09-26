---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: ユーザー アカウントACCT_BIN UID を含む新しい構造をExchangeします。
ms.openlocfilehash: 37718121de2aa8937dd9f1b78244d8da6fc0b662
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631140"
---
# <a name="prop_mapi_emsmdb_uid"></a>PROP_MAPI_EMSMDB_UID

アカウントの UID [ACCT_BIN](acct_bin.md)含む、新しい構造をExchangeします。 
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x2009  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ:  <br/> |0x20090102  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。
  
アカウント[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)アカウントである場合は、アカウントを使用してExchangeします。 その場合 **、PROP \_ MAPI_EMSMDB_UID** は、ACCT_BINアカウントの一意の ID である **emsmdbUID** を含むExchangeです。 アカウントがアカウントのアカウントExchange、このプロパティは未定義です。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [複数のアカウントExchange使用する](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [PidTagExchangeProfileSectionId ���K���̃v���p�e�B](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)


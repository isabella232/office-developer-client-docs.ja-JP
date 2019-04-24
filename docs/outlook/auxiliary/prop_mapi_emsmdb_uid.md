---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Exchange アカウントの UID を含む ACCT_BIN 構造体を表します。
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326552"
---
# <a name="propmapiemsmdbuid"></a>PROP_MAPI_EMSMDB_UID

Exchange アカウントの UID を含む[ACCT_BIN](acct_bin.md)構造体を表します。 
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x2009  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティタグ:  <br/> |0x20090102  <br/> |
|接続  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>解説

[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。
  
[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)を使用して、アカウントが Exchange アカウントであるかどうかを確認します。 その場合、 **PROP\_MAPI_EMSMDB_UID**は、Exchange アカウントの一意の ID である**emsmdbUID**を含む**ACCT_BIN**です。 アカウントが Exchange アカウントではない場合、このプロパティは未定義です。
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [複数の Exchange アカウントの使用](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [PidTagExchangeProfileSectionId ���K���̃v���p�e�B](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)


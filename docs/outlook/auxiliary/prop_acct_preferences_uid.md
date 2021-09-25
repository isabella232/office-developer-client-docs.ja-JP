---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: アカウントの基本設定を格納するプロファイル セクションの一意識別子 (UID) を取得します。
ms.openlocfilehash: 34c781f4a6a1692416f4a33b7cc34ebcf3375c9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625638"
---
# <a name="prop_acct_preferences_uid"></a>PROP_ACCT_PREFERENCES_UID

アカウントの基本設定を格納するプロファイル セクションの一意識別子 (UID) を取得します。 
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0022  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ:  <br/> |0x00220102  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IMAPISupport::OpenProfileSection](https://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx)への呼び出しで、アカウントの基本設定を含むプロファイル セクションを取得するには、PROP_ACCT_PREFERENCES_UIDを使用します。  
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [スパム対策の設定について](about-anti-spam-settings.md)


---
title: PROP_ACCT_PREFERENCES_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ec0aac33-624e-48f7-8177-8f7b8db6af7d
description: アカウントの基本設定を格納するプロファイル] セクションに一意の識別子 (UID) を取得します。
ms.openlocfilehash: 70e61264e5525f26e9f52e402bc785b544a0b90e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799572"
---
# <a name="propacctpreferencesuid"></a>PROP_ACCT_PREFERENCES_UID

アカウントの基本設定を格納するプロファイル] セクションに一意の識別子 (UID) を取得します。 
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0022  <br/> |
|プロパティの種類:  <br/> |PT_BINARY  <br/> |
|プロパティ タグ。  <br/> |0x00220102  <br/> |
|アクセス:  <br/> |値の取得のみ可能です。  <br/> |
   
## <a name="remarks"></a>備考

[IMAPISupport::OpenProfileSection](http://msdn.microsoft.com/library/cd1fa994-9531-46c4-94e5-505e7f90b884%28Office.15%29.aspx)への呼び出しで**PROP_ACCT_PREFERENCES_UID**を使用すると、アカウントの基本設定を含むプロファイル セクションを取得します。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)
- [スパム対策の設定について](about-anti-spam-settings.md)

---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: SMTP アカウントに使用する暗号化された接続の種類を指定します。
ms.openlocfilehash: eb267e71f63bd02dc0268e06f62b288f56e4db11
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592733"
---
# <a name="prop_smtp_secure_connection"></a>PROP_SMTP_SECURE_CONNECTION

SMTP アカウントに使用する暗号化された接続の種類を指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|識別子:  <br/> |0x020A  <br/> |
|プロパティの種類:  <br/> |PT_DWORD  <br/> |
|プロパティ タグ:  <br/> |0x020A0003  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

値には、次のいずれかの定数を指定できます。 値 [については、「定数 (アカウント管理 API)」](constants-account-management-api.md) を参照してください。 
  
|**Constants**|**説明**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |暗号化は使用しません。  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Secure Socket Layer (SSL) 暗号化を使用します。  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |トランスポート層セキュリティ (TLS) 暗号化および認証プロトコルを使用します。  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |メール サーバーでサポートされている暗号化方法を自動的に検出して使用します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


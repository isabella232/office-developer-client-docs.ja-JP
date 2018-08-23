---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: SMTP アカウントに使用する暗号化された接続の種類を指定します。
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799579"
---
# <a name="propsmtpsecureconnection"></a>PROP_SMTP_SECURE_CONNECTION

SMTP アカウントに使用する暗号化された接続の種類を指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|識別子:  <br/> |0x020A  <br/> |
|プロパティの種類:  <br/> |PT_DWORD  <br/> |
|プロパティ タグ。  <br/> |0x020A0003  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

値には、以下の定数のいずれかを指定できます。 その値の[定数 (アカウント管理 API)](constants-account-management-api.md)を参照してください。 
  
|**定数**|**説明**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |暗号化を使用しません。  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |セキュア ソケット レイヤー (SSL) 暗号化を使用します。  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |トランスポート層セキュリティ (TLS) の暗号化および認証プロトコルを使用します。  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |自動的に検出し、メール サーバーでサポートされている暗号化方式を使用します。  <br/> |
   
## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


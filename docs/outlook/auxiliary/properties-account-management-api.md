---
title: (アカウント管理 API) のプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: このセクションでは、アカウント管理 API のプロパティについて説明します。
ms.openlocfilehash: abf7422d941f581f66a118c35d2b6ff3c03e8b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799609"
---
# <a name="properties-account-management-api"></a>(アカウント管理 API) のプロパティ

このセクションでは、アカウント管理 API のプロパティについて説明します。
  
|**プロパティ**|**説明**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |これは、メッセージのサブ アカウントの「送信」スタンプです。  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |これは、メッセージをプライマリ アカウントの「送信」スタンプです。  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |アカウントの既定の配信フォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |アカウントの既定の配信ストアのエントリ ID を表します。  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |アカウントが作成されるプロファイル内のアカウントを一意に識別する識別子を返します。  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |アカウントが Exchange アカウントの場合は true。  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Outlook プロファイル間で一意であるアカウントの識別子を返します。  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |アカウント名を設定または返します。  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |アカウントの基本設定を格納するプロファイル] セクションに一意の識別子 (UID) を取得します。  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |アカウントの「送信」タイムスタンプをを返します。  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |アカウントの送信済みアイテムの既定のフォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |アカウントのタイムスタンプを返します。  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |アカウントの電子メール アドレスを指定します。  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |ユーザーの表示名を設定または返します。  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |一般的なインターネット メールボックスのユーザーのパスワードを表します。  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |一般的なインターネット メールボックスのポート番号を表します。  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |一般的なインターネット メールボックスのサーバー名を表します。  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |一般的なインターネット メールボックスのセキュア ソケット レイヤー (SSL) を使用するかどうかを指定します。  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |一般的なインターネット メールボックスのセキュリティで保護されたパスワード認証 (SPA) を使用するかどうかを指定します。  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |一般的なインターネット メールボックスのユーザー名を表します。  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Exchange アカウントの UID を含む[ACCT_BIN](acct_bin.md)構造体を表します。  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |取得または、アカウントのアドレス帳のエントリ ID を設定します。  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Outlook を使用して必要な同期タスクを決定し、アカウントをサポートしないユーザー インターフェイス (UI) 要素を無効にするトランスポートの設定を表します。  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |POP アカウントのサーバーにメッセージのコピーを残すかを指定します。  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |SMTP アカウントに使用する認証方法を指定します。  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |SMTP アカウントのパスワードを表します。  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |SMTP のポート番号を表します。  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |SMTP アカウントに使用する暗号化された接続の種類を指定します。  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |SMTP アカウントのサーバー名を表します。  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |SMTP アカウントのセキュア ソケット レイヤー (SSL) プロトコルを使用するかどうかを指定します。  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |SMTP アカウントの認証を使用するかどうかを指定します。  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |SMTP アカウントのセキュリティで保護されたパスワード認証 (SPA) を使用するかどうかを指定します。  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |SMTP アカウントのユーザー名を表します。  <br/> |
   

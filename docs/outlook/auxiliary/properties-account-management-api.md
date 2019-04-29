---
title: プロパティ (アカウント管理 API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: このセクションでは、アカウント管理 API のプロパティについて説明します。
ms.openlocfilehash: d0b8c06716bd2f3a3bb2941e098bd9f11ab87183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416336"
---
# <a name="properties-account-management-api"></a>プロパティ (アカウント管理 API)

このセクションでは、アカウント管理 API のプロパティについて説明します。
  
|**プロパティ**|**説明**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |これは、メッセージのセカンダリアカウントの "send" スタンプです。  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |これは、メッセージのプライマリアカウント "send" スタンプです。  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |アカウントの既定の配信フォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |アカウントの既定の配信ストアのエントリ ID を表します。  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |アカウントが作成されたプロファイル内のアカウントを一意に識別する識別子を返します。  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |アカウントが Exchange アカウントの場合は True。  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Outlook プロファイル全体で一意のアカウント識別子を返します。  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |アカウント名を設定または返します。  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |アカウントの設定を格納するプロファイルセクションの一意識別子 (UID) を取得します。  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |アカウント "send" スタンプを返します。  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |アカウントの送信アイテムの既定のフォルダーのエントリ ID を表します。  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |アカウントスタンプを返します。  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |アカウントの電子メールアドレスを指定します。  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |ユーザーの表示名を設定または返します。  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |一般的なインターネットメールボックスのユーザーパスワードを表します。  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |一般的なインターネットメールボックスのポート番号を表します。  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |一般的なインターネットメールボックスのサーバー名を表します。  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |一般的なインターネットメールボックスに Secure Socket Layer (SSL) を使用するかどうかを指定します。  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |一般的なインターネットメールボックスにセキュリティで保護されたパスワード認証 (SPA) を使用するかどうかを指定します。  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |一般的なインターネットメールボックスのユーザー名を表します。  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Exchange アカウントの UID を含む[ACCT_BIN](acct_bin.md)構造体を表します。  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |アカウントのアドレス帳エントリ ID を取得または設定します。  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |必要な同期タスクを決定するために Outlook で使用するトランスポート設定を表し、アカウントがサポートしていないユーザーインターフェイス (UI) 要素を無効にします。  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |POP アカウントのサーバーにメッセージのコピーを残すことを指定します。  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |SMTP アカウントに使用する認証方法を指定します。  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |SMTP アカウントのパスワードを表します。  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |SMTP アカウントのポート番号を表します。  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |SMTP アカウントに使用する暗号化された接続の種類を指定します。  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |SMTP アカウントのサーバー名を表します。  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |SMTP アカウントに Secure Socket Layer (SSL) プロトコルを使用するかどうかを指定します。  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |SMTP アカウントの認証を使用するかどうかを指定します。  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |SMTP アカウントに対してセキュリティで保護されたパスワード認証 (SPA) を使用するかどうかを指定します。  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |SMTP アカウントのユーザー名を表します。  <br/> |
   


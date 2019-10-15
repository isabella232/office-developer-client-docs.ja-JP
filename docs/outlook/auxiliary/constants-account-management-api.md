---
title: 定数 (アカウント管理 API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2a15e5df-b8e3-9c37-b1ee-2881d010e30b
description: このトピックでは、アカウント管理 API の定数の定義、クラス識別子、およびインターフェイス識別子について説明します。
ms.openlocfilehash: d36116e30eb7879dcd0db0523be8f28bb8fe82a7
ms.sourcegitcommit: adcf409d56b6cb25be6117f09794defa41ad6c0f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2019
ms.locfileid: "37495314"
---
# <a name="constants-account-management-api"></a>定数 (アカウント管理 API)

このトピックでは、アカウント管理 API の定数の定義、クラス識別子、およびインターフェイス識別子について説明します。
  
## <a name="constants"></a>定数

|**定数**|**定義**|
|:-----|:-----|
|ACCT_INIT_NOSYNCH_MAPI_ACCTS  <br/> |0x00000001  <br/> |
|ACCT_INIT_NO_STORES_CHECK  <br/> |0x00000002  <br/> |
|ACCT_INIT_NO_NOTIFICATIONS <br/> |0x00000004 <br/> |
|ACCTUI_NO_WARNING  <br/> |0x0100  <br/> |
|ACCTUI_SHOW_ACCTWIZARD  <br/> |0x0400  <br/> |
|ACCTUI_SHOW_DATA_TAB  <br/> |0x0200  <br/> |
|E_ACCT_NOT_FOUND  <br/> |0x800C8101  <br/> |
|E_ACCT_UI_BUSY  <br/> |0x800C8102  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |0x800C8105  <br/> |
|E_INVALIDARG  <br/> | *Windows Software Development Kit (SDK) ヘッダーファイル winerror.h で定義されているとおりです。*  <br/> |
|E_NOTIMPL  <br/> | *Windows SDK ヘッダーファイル winerror.h で定義されています。*  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |0x800C8002  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |0x800C8005  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |0x800C8003  <br/> |
|E_OLK_PROP_READ_ONLY  <br/> |0x800C800D  <br/> |
|E_OLK_REGISTRY  <br/> |0x800C8001  <br/> |
|ENCRYPT_ で始まる次の定数は、暗号化された接続の種類を指定するために[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md)プロパティで使用されます。  <br/> ||
|ENCRYPT_CONN_AUTO  <br/> |1/3  <br/> |
|ENCRYPT_CONN_NO_SECURITY  <br/> |.0  <br/> |
|ENCRYPT_CONN_SSL  <br/> |1-d  <br/> |
|ENCRYPT_CONN_TLS  <br/> |pbm-2  <br/> |
|MAPIACCT_SEND_ONLY  <br/> |0x00000001  <br/> |
|NOTIFY_ACCT_CHANGED  <br/> |1-d  <br/> |
|NOTIFY_ACCT_CREATED  <br/> |pbm-2  <br/> |
|NOTIFY_ACCT_DELETED  <br/> |1/3  <br/> |
|NOTIFY_ACCT_ORDER_CHANGED  <br/> |4   <br/> |
|NOTIFY_ACCT_PREDELETED  <br/> |5   <br/> |
|OLK_ACCOUNT_NO_FLAGS  <br/> |.0  <br/> |
|S_OK  <br/> | *Windows SDK ヘッダーファイル winerror.h で定義されています。*  <br/> |
|S_FALSE  <br/> | *Windows SDK ヘッダーファイル winerror.h で定義されています。*  <br/> |
|SECURE_FLAG  <br/> |0x8000  <br/> |
|SMTP_ で始まる次の定数は、 [PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md)プロパティで使用され、認証方法を指定します。  <br/> ||
|SMTP_AUTH_SAME_AS_POP  <br/> |.0  <br/> |
|SMTP_AUTH_RECEIVE_BEFORE_SEND  <br/> |pbm-2  <br/> |
|SMTP_AUTH_USER_PASS  <br/> |1-d  <br/> |
|次の5つの定数とマクロは、 [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md)プロパティで使用され、サーバー上にメッセージのコピーを残す POP アカウントのオプションを指定します。  <br/> ||
|LEAVE_ON_SERVER  <br/> |0x1  <br/> |
|REMOVE_AFTER  <br/> |0x2  <br/> |
|REMOVE_ON_NUKE  <br/> |0x4  <br/> |
|GET_REMOVE_AFTER_DAYS (ul)  <br/> |((ul)\>\>16)  <br/> |
|SET_REMOVE_AFTER_DAYS (日数)  <br/> |((日数)\<\<16)  <br/> |
   
## <a name="class-identifiers"></a>クラス識別子

Windows SDK ヘッダーファイルの guiddef で定義されている DEFINE_GUID マクロを使用して、GUID シンボリック名とその値を関連付けます。
  
{ed475410-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkAccountManager、0xed475410、0xb・ 6、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76); 
  
{ed475411-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkPOP3Account、0xed475411、0xbkbs 6、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76);
  
{ed475412-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkIMAP4Account、0xed475412、0xbkbs 6、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76);
  
{ed475414-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkMAPIAccount、0xed475414、0xbkbs 6、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76);
  
{ed475418-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkMail、0xed475418、0xbkbs 6、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76);
  
{ed475419-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkAddressBook、0xed475419、0xb・ 6、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76);
  
{ed475420-b0d6-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (CLSID_OlkStore、0xed475420、0xbkbs 6、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76);
  
{4db5cbf0-3b77-4852-bc8e-bb81908861f3}
  
DEFINE_GUID (CLSID_OlkHotmailAccount、0x4db5cbf0、0x3b77、0x4852、0xbc、0x8e、0xbc、0x81、0xbc、0x8e、0x61、0xf3)。
  
{4db5cbf2-3b77-4852-bc8e-bb81908861f3}
  
DEFINE_GUID (CLSID_OlkLDAPAccount、0x4db5cbf2、0x3b77、0x4852、0xbc、0x8e、0xbc、0x81、0xbc、0x8e、0x61、0xf3)。
  
## <a name="interface-identifiers"></a>インターフェイス識別子

Windows SDK ヘッダーファイルの guiddef で定義されている DEFINE_GUID マクロを使用して、GUID シンボリック名とその値を関連付けます。
  
{9240A6C0-AF41-11d2-8C3B-00104B2A6676}
  
DEFINE_GUID (IID_IOlkErrorUnknown, 0x9240a6c0、0xaf41、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76);
  
{9240A6C1-AF41-11d2-8C3B-00104B2A6676}
  
DEFINE_GUID (IID_IOlkEnum, 0x9240a6c1、0xaf41、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76);
  
{9240a6c3-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountNotify, 0x9240a6c3、0xaf41、0x11d2、0x8c、0x3b、0x0、0x10、0x4b、0x2a、0x66、0x76);
  
{9240a6cb-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountHelper, 0x9240a6cb, 0xaf41, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0x2a, 0x66, 0x76); 
  
{9240a6cd-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccountManager, 0x9240a6cd, 0xaf41, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0x2a, 0x66, 0x76); 
  
{9240a6d2-af41-11d2-8c3b-00104b2a6676}
  
DEFINE_GUID (IID_IOlkAccount, 0x9240a6d2, 0xaf41, 0x11d2, 0x8c, 0x3b, 0x0, 0x10, 0x4b, 0x2a, 0x66, 0x76);
  


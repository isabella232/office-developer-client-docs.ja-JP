---
title: MAPI アドレスの種類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 20eb429b2574f67e8b28ae96eeb96f42840123d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801312"
---
# <a name="mapi-address-types"></a>MAPI アドレスの種類

  
  
**適用されます**: Outlook 
  
メッセージングのすべてのユーザーは、アドレスの種類、 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) のプロパティに格納されているユーザーのアドレスの形式を記述する文字の文字列に関連付けられます。 アドレスの種類は、アドレスの形式にマップします。 受信者のアドレスの種類を見ると、により、クライアント アプリケーションは、受信者に適切なアドレスの書式を設定する方法を決定できます。 
  
などの`SMTP`のアドレスの種類は、標準的なインターネット アドレスを指定します。 
  
 `username@companyname.com.`
  
`EX`のアドレスの種類は、Exchange Server のアドレスを指定します。 
  
すべてのアドレス帳のエントリには、有効なアドレスの種類が必要です。 クライアントでは、ユーザーのカスタム受信者のアドレス帳プロバイダーでサポートされていない型を作成するときに、アドレスの種類を指定する必要があります。 、それらをサポートしているエントリのアドレス帳プロバイダーは、有効なアドレスの種類を指定する必要があります。 
  
MAPI のみ 1 つのアドレスの種類を定義する: MAPIPDL は、個人用配布リストを意味します。
  
セッションのすべてのトランスポート プロバイダーによってサポートされているアドレスの種類の一覧を取得するには、クライアント アプリケーションは、 **IMAPISession::EnumAdrTypes**メソッドを呼び出します。 詳細については、 [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)を参照してください。
  


---
title: MAPI アドレスの種類
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298013"
---
# <a name="mapi-address-types"></a>MAPI アドレスの種類

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのメッセージングユーザーは、 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティに格納されているユーザーのアドレスの形式を示す文字列であるアドレスの種類に関連付けられています。 アドレスの種類は、アドレス形式にマップされます。 つまり、受信者のアドレスの種類を調べることで、クライアントアプリケーションは受信者に適したアドレスを書式設定する方法を判断できます。 
  
たとえば、アドレスの`SMTP`種類は標準のインターネットアドレスを指定します。 
  
 `username@companyname.com.`
  
そして、アドレス`EX`の種類は、Exchange サーバーのアドレスを指定します。 
  
すべてのアドレス帳エントリには、有効なアドレスの種類を指定する必要があります。 クライアントは、アドレス帳プロバイダーによってサポートされていない種類のカスタム受信者を作成するときに、ユーザーにアドレスの種類を指定するよう要求します。 サポートされているエントリについては、アドレス帳プロバイダーが有効なアドレスの種類を提供する必要があります。 
  
MAPI では、個人用配布リストを表すアドレスの種類として、mapipdl が1つだけ定義されています。
  
セッション内のすべてのトランスポートプロバイダーでサポートされているアドレスの種類の一覧を取得するために、クライアントアプリケーションは**imapisession:: enumadrtypes**メソッドを呼び出します。 詳細については、「 [imapisession:: enumadrtypes](imapisession-enumadrtypes.md)」を参照してください。
  


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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405437"
---
# <a name="mapi-address-types"></a>MAPI アドレスの種類

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのメッセージング ユーザーは、PR_ADDRTYPE **(** [PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティに格納されているユーザーのアドレスの形式を表す文字列であるアドレスの種類に関連付けます。 アドレスの種類は、アドレス形式にマップされます。 つまり、受信者のアドレスの種類を確認することで、クライアント アプリケーションは、受信者に適したアドレスを書式設定する方法を決定できます。 
  
たとえば、アドレスの  `SMTP` 種類は、標準のインターネット アドレスを指定します。 
  
 `username@companyname.com.`
  
また、アドレス `EX` の種類は、アドレスのExchange Serverします。 
  
すべてのアドレス帳エントリには、有効なアドレスの種類が必要です。 クライアントは、アドレス帳プロバイダーでサポートされていない種類のカスタム受信者を作成するときに、ユーザーにアドレスの種類を指定する必要があります。 サポートするエントリについては、有効なアドレスの種類を指定するためにアドレス帳プロバイダーが必要です。 
  
MAPI では、個人配布リストを表す MAPIPDL という 1 つのアドレスの種類のみを定義します。
  
セッション内のすべてのトランスポート プロバイダーでサポートされているアドレスの種類の一覧を取得するには、クライアント アプリケーションは **IMAPISession::EnumAdrTypes** メソッドを呼び出します。 詳細については [、「IMAPISession::EnumAdrTypes」を参照してください](imapisession-enumadrtypes.md)。
  


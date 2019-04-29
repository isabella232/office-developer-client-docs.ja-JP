---
title: PROP_SMTP_SSL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f46e8aa3-d2c2-45a2-93fe-1c40107fbf16
description: SMTP アカウントに Secure Socket Layer (SSL) プロトコルを使用するかどうかを指定します。
ms.openlocfilehash: 64856322ec0afce80777417f781c22b927ed5e2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407075"
---
# <a name="propsmtpssl"></a>PROP_SMTP_SSL

SMTP アカウントに Secure Socket Layer (SSL) プロトコルを使用するかどうかを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|識別子:  <br/> |0x0202  <br/> |
|プロパティの種類:  <br/> |PT_DWORD  <br/> |
|プロパティタグ:  <br/> |0x02020003  <br/> |
|接続  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

ゼロ値は、ssl 暗号化を使用しないことを意味します。それ以外の場合は ssl 暗号化を使用します。
  
## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md) 
- [定数 (アカウント管理 API)](constants-account-management-api.md)


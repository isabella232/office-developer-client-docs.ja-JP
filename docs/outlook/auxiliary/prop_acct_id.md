---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: アカウントが作成されたプロファイル内のアカウントを一意に識別する識別子を返します。
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407166"
---
# <a name="propacctid"></a>PROP_ACCT_ID

アカウントが作成されたプロファイル内のアカウントを一意に識別する識別子を返します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0001  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|プロパティタグ:  <br/> |0x00010003  <br/> |
|接続  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。 クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。 
  
このプロパティは、アカウントが作成されたプロファイル内のすべてのアカウント間で一意に識別されるという点で、 [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md)とは異なりますが、 **PROP\_ACCT_MINI_UID**は内のアカウントを一意に識別します。アカウントが作成されたプロファイルの外部。 これらのプロパティを持つメッセージが、異なる Outlook プロファイルおよび異なるアカウントのセットを持つ2番目のコンピューターに移動する場合、 **PROP_ACCT_ID**は2番目のコンピューターのプロファイルのアカウントと競合する可能性があります。 **PROP_ACCT_MINI_UID**元のプロファイルで元のアカウントを一意に識別することができます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)


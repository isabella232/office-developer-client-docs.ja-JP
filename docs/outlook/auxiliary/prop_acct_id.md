---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: アカウントが作成されるプロファイル内のアカウントを一意に識別する識別子を返します。
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407166"
---
# <a name="prop_acct_id"></a>PROP_ACCT_ID

アカウントが作成されるプロファイル内のアカウントを一意に識別する識別子を返します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
|||
|:-----|:-----|
|識別子:  <br/> |0x0001  <br/> |
|プロパティの種類:  <br/> |PT_LONG  <br/> |
|プロパティ タグ:  <br/> |0x00010003  <br/> |
|アクセス:  <br/> |読み取り専用  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。 クライアントがこのプロパティを設定しようとすると、このプロパティは次 **E_OLK_PROP_READ_ONLY。** 
  
このプロパティは [、PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) とは異なりますが、その値は、アカウントが作成されたプロファイル内のすべてのアカウント間でのみ一意ですが **、PROP \_ ACCT_MINI_UID** はアカウントが作成されたプロファイルの中と外側のアカウントを一意に識別します。 これらのプロパティを持つメッセージが別の Outlook プロファイルと異なるアカウント セットを持つ 2 番目のコンピューターにローミングすると **、PROP_ACCT_ID** は 2 番目のコンピューターのプロファイル内のアカウントと競合する可能性があります **。PROP_ACCT_MINI_UID** は元のプロファイルの元のアカウントを一意に識別できます。 
  
## <a name="see-also"></a>関連項目

- [アカウント管理 API について](about-the-account-management-api.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)


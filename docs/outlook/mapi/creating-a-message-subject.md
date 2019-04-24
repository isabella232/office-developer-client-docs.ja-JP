---
title: メッセージの件名の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332964"
---
# <a name="creating-a-message-subject"></a>メッセージの件名の作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの件名 ([PidTagSubject](pidtagsubject-canonical-property.md)) **** はオプションのプロパティで、メッセージの目的を要約するために使用されます。 この設定を選択した場合は、文字列128バイト以下にしてください。 128バイト制限は、MAPI の制限ではありません。一部のメッセージストアプロバイダーによって課される制限です。 適用されるプロバイダーとの相互運用性を確保するには、件名を128バイトに制限します。 
  
一部のメッセージストアプロバイダーでは、 **PR_SUBJECT**を[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスを使用した stream に書き込むことが許可されていないことに注意してください。 
  
**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) を設定しません。このプロパティは、返信メッセージと転送メッセージに対してのみ設定されます。 
  


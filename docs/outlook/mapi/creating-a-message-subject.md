---
title: メッセージ件名の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b5ae0c8e16af35b730d6a1fbdcf95b74c6119e1b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631074"
---
# <a name="creating-a-message-subject"></a>メッセージ件名の作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの件名である PR_SUBJECT **(** [PidTagSubject)](pidtagsubject-canonical-property.md)は、メッセージの意図を要約するために使用されるオプションのプロパティです。 設定する場合は、文字列を 128 バイト以下にしてください。 128 バイトの制限は、MAPI によって課される制限ではありません。これは、一部のメッセージ ストア プロバイダーによって課される制限です。 これを行うプロバイダーとの相互運用性を確保するには、サブジェクトを 128 バイトに制限します。 
  
一部のメッセージ ストア プロバイダーでは、IStream インターフェイスPR_SUBJECTストリームへの書き込みが許可されていない[場合](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)があります。  
  
[設定しない **] PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md));このプロパティは、返信と転送されたメッセージにのみ設定されます。 
  


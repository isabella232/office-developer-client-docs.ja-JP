---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427137"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**attAttachRenddata** 属性は、メッセージ テキストで添付ファイルがレンダリングされる方法と場所を説明する **RENDDATA** 構造としてエンコードされます。 **RENDDATA** 構造体は、RENDDATA 構造体の最初のメンバーで始まる **sizeof(RENDDATA)** バイトとして **TNEF** ストリームでエンコードされます。 **RENDDATA** 構造体の **dwFlags** メンバーの値が **MAC_BINARY** に設定されている場合、次の添付ファイルのデータは MacBinary 形式で格納されます。それ以外の場合、添付ファイル データは通常どおりエンコードされます。
  


---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a21f6ca242f07abf865885794cf71f0ff3135eba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605175"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**attAttachRenddata** 属性は、メッセージ テキストで添付ファイルがレンダリングされる方法と場所を説明する **RENDDATA** 構造としてエンコードされます。 **RENDDATA** 構造体は、RENDDATA 構造体の最初のメンバーで始まる **sizeof(RENDDATA)** バイトとして **TNEF** ストリームでエンコードされます。 **RENDDATA** 構造体の **dwFlags** メンバーの値が **MAC_BINARY** に設定されている場合、次の添付ファイルのデータは MacBinary 形式で格納されます。それ以外の場合、添付ファイル データは通常どおりエンコードされます。
  


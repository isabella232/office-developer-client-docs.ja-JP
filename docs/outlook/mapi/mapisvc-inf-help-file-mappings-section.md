---
title: MapiSvc.inf [ヘルプ ファイルのマッピング] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 776f797d0c96d9173e114fd499d6cca0494a0a43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801534"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>MapiSvc.inf [ヘルプ ファイルのマッピング] セクション

  
  
**適用されます**: Outlook 
  
**[ヘルプ ファイルのマッピング]** セクションには、サービスによって生成されるエラーのヘルプを提供するファイルを 1 つのメッセージ サービスをマップの各エントリが含まれています。 このセクションのエントリは、次の形式を使用します。 
  
 **[ファイルのマッピングを支援する]**_メッセージ サービス名_ =  _ヘルプ ファイル名]_
  
メッセージ サービス名は、インストールされているメッセージ サービスの名前ヘルプ ファイル名は、エラー情報が格納されているファイルの名前です。 例を次の 3 つのサービスのエントリが含まれている標準的な **[ヘルプ ファイルのマッピング]** セクションを示しています: MAPI、MsgService サービス、および MS サービスです。 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```



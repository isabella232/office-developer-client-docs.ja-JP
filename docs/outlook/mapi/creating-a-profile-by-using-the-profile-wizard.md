---
title: プロファイル ウィザードを使用してプロファイルを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799857"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>プロファイル ウィザードを使用してプロファイルを作成します。

  
  
**適用されます**: Outlook 
  
プロファイル ウィザードは、可能な最も簡単な方法でプロファイルを作成するユーザーを有効にする MAPI 機能です。 プロファイル ウィザードでは、一連のメッセージ サービスを選択し、いくつかの最も重要な構成プロパティの値を入力するように求めるダイアログ ボックスが表示されます。 その他の必要なプロパティのほとんどは、プロファイル ウィザードは、既定値を使用します。 プロファイル ウィザードを起動するには、 **LaunchWizard**、 [LAUNCHWIZARDENTRY](launchwizardentry.md)のプロトタイプでは関数を呼び出します。 
  
ユーザーは、プロファイル ウィザードをサポートする新しいプロファイルに、メッセージ サービスとサービス ・ プロバイダーだけを追加できます。 各メッセージ サービスでは、プロファイル ウィザードが処理できるよりもを設定するその他のプロパティに必要なために、このアプローチを使用する場合ことが、選択したサービスまたは構成が不完全なのでプロバイダーの 1 つ以上に注意します。
  


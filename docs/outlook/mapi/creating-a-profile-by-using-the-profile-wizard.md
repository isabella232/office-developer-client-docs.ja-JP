---
title: プロファイル ウィザードを使用したプロファイルの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f30dca8323f74bc2817bab375b58fcc1bc15c18b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574259"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>プロファイル ウィザードを使用したプロファイルの作成

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロファイル ウィザードは、可能な最も簡単な方法でプロファイルを作成するユーザーを有効にする MAPI 機能です。 プロファイル ウィザードでは、一連のメッセージ サービスを選択し、いくつかの最も重要な構成プロパティの値を入力するように求めるダイアログ ボックスが表示されます。 その他の必要なプロパティのほとんどは、プロファイル ウィザードは、既定値を使用します。 プロファイル ウィザードを起動するには、 **LaunchWizard**、 [LAUNCHWIZARDENTRY](launchwizardentry.md)のプロトタイプでは関数を呼び出します。 
  
ユーザーは、プロファイル ウィザードをサポートする新しいプロファイルに、メッセージ サービスとサービス ・ プロバイダーだけを追加できます。 各メッセージ サービスでは、プロファイル ウィザードが処理できるよりもを設定するその他のプロパティに必要なために、このアプローチを使用する場合ことが、選択したサービスまたは構成が不完全なのでプロバイダーの 1 つ以上に注意します。
  


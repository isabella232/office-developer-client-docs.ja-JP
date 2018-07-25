---
title: カスタム アセンブリを追加および参照する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003 互換のフォーム テンプレート,カスタム アセンブリを使用する,アセンブリ [InfoPath 2007],InfoPath 2003 オブジェクト モデルを使用してカスタムを追加する
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: マネージ コードのフォーム テンプレート プロジェクトでカスタム アセンブリへの参照を追加すると、プロジェクトをコンパイルおよび発行したときに、そのアセンブリがフォーム テンプレート ファイル (.xsn) に含められます。
ms.openlocfilehash: e182930ebe14b6f64d1b90509fe400cc1fb1b26e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799107"
---
# <a name="add-and-reference-custom-assemblies"></a>カスタム アセンブリを追加および参照する

マネージ コードのフォーム テンプレート プロジェクトでカスタム アセンブリへの参照を追加すると、プロジェクトをコンパイルおよび発行したときに、そのアセンブリがフォーム テンプレート ファイル (.xsn) に含められます。
  
## <a name="add-and-reference-a-custom-assembly"></a>カスタム アセンブリを追加および参照する

InfoPath プロジェクト システムがフォーム テンプレート ファイルに追加されるファイルを管理する方法と競合しないように、フォーム テンプレート プロジェクトの最上位フォルダーには、参照するカスタム アセンブリをコピーしないでください。既定では、このフォルダーのパス形式は < *drive*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName*  となります。 
  
参照するカスタム アセンブリをプロジェクト フォルダー内で移動するには、メイン プロジェクト フォルダーの下にサブフォルダーを作成し、そのサブフォルダーにコピーしたカスタム アセンブリを参照する必要があります。ただし、参照するアセンブリのためのサブフォルダーを作成する必要はありません。参照するアセンブリがプロジェクトの最上位フォルダーになければ、プロジェクトをコンパイルおよび発行したときに、InfoPath プロジェクト システムによってアセンブリがフォーム テンプレート ファイル (.xsn) にコピーされます。
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a>既定の場所からカスタム アセンブリを参照する

1. Visual Studio 2012 でフォーム テンプレート プロジェクトを開きます。
    
2. [ **プロジェクト**] メニューで、[ **参照の追加**] をクリックします。
    
3. [ **参照**] タブで、アセンブリを探して選択し、[ **OK**] をクリックして参照を追加します。 
    
## <a name="see-also"></a>関連項目

#### <a name="tasks"></a>タスク

[InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートを作成する](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)


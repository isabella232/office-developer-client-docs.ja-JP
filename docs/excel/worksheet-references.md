---
title: ワークシートの参照
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- references [excel 2007], worksheet,worksheet references [Excel 2007],external worksheet references [Excel 2007],active worksheet [Excel 2007],current worksheet [Excel 2007],internal worksheet references [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: b7089fb891c96be9182189e3a5f30057721cebbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798966"
---
# <a name="worksheet-references"></a>ワークシートの参照

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel における参照とは、長方形のセル ブロック (1 セルのみの場合もある) を参照するデータ型を指します。または、複数の離散したセル ブロックを参照する場合もあります。 Excel 内部では、現在のシート上のセルに 1 つの参照型を使用します。これは内部参照として知られています。 現在のシートに含まれていないあらゆるセルは、外部参照とも呼ばれる、もう 1 つの参照型で表します。 「作業中」と「現在」の定義については、次のセクションを参照してください。
  
## <a name="active-vs-current"></a>作業中と現在

Excel での「作業中」という用語は、ユーザーが表示しているものを指しています。作業中のブックやシートは、ユーザーが現在閲覧中のブックやワークシート、または Excel から別アプリケーションにフォーカスが移った場合には、Excel で最後にフォーカスしていた際に表示していたブックやワークシートを指します。作業中のシートは、必ず作業中のブック内にあります。作業中のシート内で複数のセルが選択されている場合は、アクティブ セルとして認識されます。埋め込みオブジェクトにフォーカスされている場合は、最後に選択したセルが引き続きアクティブになります。 
  
「現在」という用語は、Excel が計算しているものを指します。現在のブックとワークシートは、現在再計算を行っているブックやワークシートを指します。現在のシートは、必ず現在のブック内にあります。再計算されているセルは現在のセルと呼ばれます。また、配列数式が再計算されている場合も、現在のセルと呼ばれます。 
  
覚えておくべき重要なポイントは次のとおりです。
  
- 作業中のブックやシート、セルが、必ずしも現在のブックやシート、セルになるわけではありません (現在のものである場合もあります)。
    
- Visual Basic for Applications (VBA) モジュールや 、DLL または XLL において、アドイン関数は、現在のシート上にある現在のセルから呼び出されます。マルチ スレッド再計算 (MTR) の場合は、それらのいずれかから呼び出されます。
    
ブック内のセル、セル範囲、シートについての情報を提供する多くの Excel の関数は、作業中のブック、シート、セルと、現在のブック、シート、セルとを区別します。これらの相違点は、次のセクションに記載されているとおり、セル ブロックの参照を表すために使用するデータ型にも反映されます。
  
## <a name="internal-and-external-worksheet-references"></a>内部ワークシートおよび外部ワークシートの参照

内部参照と外部参照の主な違いは、外部参照のデータ型には、ワークシート ID に加えて、参照先セルの記述が含まれていることです。内部参照にはシートへの参照が含まれていません。シートが現在のシートであることを暗黙的に示します。 
  
多くの C API 関数は、参照を返すか、参照引数を取ります。 参照引数を取る C API 関数は、いずれも内部参照または外部参照のどちらも受け入れます。ただし、**xlSheetNm** 関数は例外であり、外部参照が必要です。 関数によっては、内部参照または外部参照のいずれか一方のみを返します。 たとえば、C API 関数 [xlfCaller](xlfcaller.md) は、定義により、現在のシート上の呼び出し元のセルへの参照を返します。 返される参照は常に内部参照になります。ただし、関数がワークシートのセルから呼び出されたのでない場合、非参照型を返す可能性があります。 C API 関数 [xlSheetId](xlsheetid.md) は、必ず外部参照データ型に含まれるワークシート ID を返します。 
  
内部参照型と外部参照型の、もう一つの主な違いは、外部参照のデータ型は同じシート上の複数の離散したセル ブロックを表すことができるという点です。内部参照では、現在のシートの 1 ブロックのみを表すことができます。離散した参照は、範囲の引数を取る任意の関数に渡すことができます。
  
## <a name="see-also"></a>関連項目



[Excel プログラミングの概念](excel-programming-concepts.md)
  
[名前と他のワークシートの数式を評価する](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Excel ワークシートと式の評価](excel-worksheet-and-expression-evaluation.md)


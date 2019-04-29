---
title: クイック ファイリング ダイアログ ボックス インタ フェース (OneNote 2013)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d83e39f0-b259-4c33-8f3e-e03e94c2403d
description: このトピックは、 OneNote 2013では、[クイック ファイリング] ダイアログ ボックスをプログラムでカスタマイズするのに使用できるインターフェイスについて説明します。
ms.openlocfilehash: dd6b28ae6cb2acb007bae26ea661facaf1f8d4be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425338"
---
# <a name="quick-filing-dialog-box-interfaces-onenote"></a>クイック ファイリング ダイアログ ボックス インタ フェース (OneNote 2013)

このトピックは、 OneNote 2013では、[クイック ファイリング] ダイアログ ボックスをプログラムでカスタマイズするのに使用できるインターフェイスについて説明します。
  
## <a name="quick-filing-dialog-box"></a>[クイックファイリング] ダイアログボックス

クイック ファイリング] ダイアログ ボックスのOneNote 2013では、OneNote の階層構造内の場所を選択できるようにするカスタマイズ可能なダイアログ ボックスです。選択可能な場所には、ノートブック、セクション グループ、セクション、ページおよびサブページが含まれます。ダイアログ ボックスは、OneNote アプリケーション内およびOneNote 2013 API を通じて、外部アプリケーションによって使用されます。図 1 は、既定の状態でクイック ファイリング] ダイアログ ボックスを示します。
  
**図 1。クイック ファイリング] ダイアログ ボックスのカスタマイズなし**

![カスタマイズのない [クイックファイリング] ダイアログボックス](media/ON15Con_quick_filing_dialog.jpg "カスタマイズのない [クイックファイリング] ダイアログボックス")
  
ユーザー、ダイアログ ボックス内の特定の場所、または、テキスト ボックスに入力することによって、OneNote ツリー構造の検索をすべてのノートブックの階層を移動できます。カスタマイズ可能なダイアログ ボックスの側面には、タイトル、説明、最近の結果のリスト、チェック ボックスのテキストと状態、ツリーの深さ、ボタン、および選択可能な場所の種類が含まれます。

クイック ファイリング ダイアログ ボックス機能はOneNote 2013の 2 つのインターフェイスを通じてアクセスできます。 **IQuickFilingDialog**インタ フェースのインスタンスを作成、設定することができます、ダイアログ ボックスを実行する. **IQuickFilingDialogCallback**インターフェイスは、ダイアログ ボックスが閉じられた後に呼び出されます。ダイアログ ボックスは、OneNote のプロセスで実行されるため、ダイアログ ボックスのスレッドの実行を維持する機構が必要にしが閉じているときに、ユーザーの選択やダイアログ ボックスの状態をキャプチャします。 
  
## <a name="iquickfilingdialog-interface"></a>iquickfilingdialog インターフェイス
<a name="odc_IQuickFilingDialog"> </a>

このインターフェイスをカスタマイズして、ダイアログ ボックスを実行することができます。ユーザーは、 **Application.QuickFilingDialog**メソッドを使用して、 **Application**クラスを使用する] ダイアログ ボックスをインスタンス化できます。このメソッドはダイアログ ボックスのインスタンスを返します。 **IQuickFilingDialog.Run**メソッドのプロパティ] ダイアログ ボックスの設定は、ダイアログ ボックスを実行する使用されます。このメソッドは、新しいスレッドで、ダイアログ ボックスを実行します。 
  
**新しいプロパティ**

|**名前**|**Type**|**説明**|
|:-----|:-----|:-----|
|**Title** <br/> |string  <br/> |取得またはダイアログ ボックス ウィンドウのタイトル バーに表示されるタイトル テキストを設定します。  <br/> |
|**Description** <br/> |string  <br/> |取得または設定、テキストの説明に何を選択するように指示します。この値は、複数行のテキストを指定できます。  <br/> |
|**CheckboxText** <br/> |string  <br/> |取得または、次のチェック ボックスのテキストを設定します。この値が空でない文字列に設定] ダイアログ ボックスで、チェック ボックスが表示されます。値は、空の文字列は、チェック ボックスは表示されません。  <br/> |
|**CheckboxState** <br/> |bool  <br/> |取得またはチェック ボックスの状態を設定します。 **false**に設定されている場合、ダイアログ ボックスを起動します] チェック ボックスは消去されます。 **true**が指定されている場合、ダイアログ ボックスの **CheckboxText**が空でない文字列が開始されると、このチェック ボックスが選択されます。 <br/> |
|**WindowHandle** <br/> |ulong  <br/> |クイック ファイリング ダイアログ ボックス ウィンドウのハンドル ID を取得します。  <br/> |
|**ツリーの深さ** <br/> |**HierarchyElement** <br/> |取得または設定、OneNote ツリー深さ、すべてのノートブック セクションに表示されます。既定では最大のセクションでは、ツリーが表示されます。このプロパティは要素の種類を選択することができます。 <br/> **TreeDepth**設定されている場合、要素をボタンのいずれかを選択できますが、OneNote の階層の下位に、表示されているツリーの深さは最も低い可能の選択可能な要素になります。つまり、ツリーの深さは、ページに表示する設定が選択可能な最小の要素は、セクション、セクションにツリーが表示されます。 <br/> |
|**ParentWindowHandle** <br/> |ulong  <br/> |取得またはダイアログ ボックスの親ウィンドウのハンドル ID を設定します。このプロパティが設定されている場合クイック ファイリング] ダイアログ ボックスになります割り当てられている親ウィンドウをモーダル ダイアログ ボックスを開くと。ユーザーはクイック ファイリング] ダイアログ ボックスが閉じられるまで、親ウィンドウにアクセスすることはできません。  <br/> |
|**Position** <br/> |tagpoint  <br/> |取得または、画面を基準にして、[ウィンドウの位置を設定します。既定では親ウィンドウまたはデスクトップの中央に、ダイアログ ボックスが表示されます。  <br/> |
|**SelectedItem** <br/> |string  <br/> |ダイアログ ボックスを閉じたときに、ユーザーが選択した OneNote の場所のオブジェクト ID を取得します。オブジェクトが設定されている場合は、ユーザーが **[キャンセル**] ボタンをクリックすると、null にします。 <br/> |
|**PressedButton** <br/> |ulong  <br/> |ダイアログ ボックスが閉じるときにクリックしてされたボタンを取得します。 **[キャンセル**] ボタンがクリックしてされた場合は、このプロパティは-1 を返します。他のすべてのボタンがダイアログ ボックスに追加のボタンごとに 1 ずつインクリメントされます、0 から整数値が割り当てられます。既定の **[ok]** ボタンの整数の値は 0 です。 <br/> |
   
### <a name="methods"></a>メソッド

**SetRecentResults**

|||
|:-----|:-----|
|**説明** <br/> |クイック ファイリング ダイアログ ボックスで、どのような最近の結果のリストが表示されますを設定していくつかの特別なファイリングの場所リストに追加するかどうかを示します。ユーザーは、 [RecentResultType](enumerations-onenote-developer-reference.md#odc_RecentResultType)列挙体からの最近の結果リストを選択できます。ユーザーは、次のオプションを一覧に追加する選択もできます。 現在のセクション、現在のページ、または落書きノート。 **RecentResultType.rrtNone**を選択すると、結果の最新のリストは表示されません。 <br/> |
|**構文** <br/> | `HRESULT SetRecentResults (`<br/>`[in]RecentResultType recentResults,`<br/>`[in]VARIANT_BOOL fShowCurrentSection,`<br/>`[in]VARIANT_BOOL fShowCurrentPage,`<br/>`[in]VARIANT_BOOL fShowUnfiledNotes);` <br/> |
|**パラメーター** <br/> | _recentResults_&ndash;最近の結果リストがある場合は、それが表示されることを示す、 **RecentResultType**型のオブジェクト。 **rrtNone**がオンの場合] ダイアログ ボックスで最新の結果のリストは表示されません。<br/><br/>  _fshowcurrentsection_&ndash;最新の結果リストに現在のセクションを含める必要があるかどうかを示すブール値。<br/><br/>  _fShowCurrentPage_&ndash;現在のページを最近の結果リストに含める必要があるかどうかを示すブール値。<br/><br/>  _fShowUnfiledNotes_&ndash; [落書きノート] セクションを最近の結果リストに含めるかどうかを示すブール値。  <br/> |
   
> [!NOTE]
> [!メモ] 特別なファイリングの場所] ダイアログ ボックスで、ボタンのいずれかで選択できません、する場合、一覧には表示されません。最近の結果の一覧で、選択可能な項目が見つからない場合、結果の最新のリストは表示されません。 
  
次の使用例は、最近の結果の一覧で、現在のセクション、現在のページと、落書きノート セクションを表示するのに、 **SetRecentResults**メソッドを使用します。 
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            ...
        }

```

**addbutton**

|||
|:-----|:-----|
|**説明** <br/> |ユーザーを追加し、ダイアログ ボックスのボタンをカスタマイズできます。ユーザーは、ボタンと各ボタンで選択できるは、OneNote の階層の要素に、テキストを指定できます。  <br/> |
|**構文** <br/> | `HRESULT AddButton (`<br/>`[in]BSTR bstrText,`<br/>`[in]HierarchyElement allowedElements,`<br/>`[in]HierarchyElement allowedReadOnlyElements,`<br/>`[in]VARIANT_BOOL fDefault);` <br/> |
|**パラメーター** <br/> | _bstrtext_&ndash;ボタンに表示するテキストを指定する文字列。 既定の **[ok]** ボタンをカスタマイズするには、null 値 **bstrText**として渡します。  <br/><br/>_allowedElements_&ndash;ユーザーがボタンを使用して選択できる、読み取り専用でない OneNote 階層要素を示す**HierarchyElement** 。 For selecting multiple items, the user should pass in the **OR** operator for all the uint equivalent values of the **HierarchyElement** types allowed as a **HierarchyElement**.<br/><br/>  _allowedReadOnlyElements_&ndash;ユーザーがボタンを使用して選択できる OneNote の読み取り専用階層要素を示す**HierarchyElement** 。 For selecting multiple items, the user should pass in the **OR** operator for all the **uint** equivalents values of the **HierarchyElement** types allowed as a **HierarchyElement**.<br/><br/>  _fdefault_&ndash;このボタンを既定のボタンにするかどうかを指定するブール値。 複数のボタンを既定値として設定した場合、最後に指定したボタンが既定のボタンになります。  <br/> |
   
次の使用例は、3 つのボタンをクイック ファイリング ダイアログ ボックス。OneNote の階層ツリー内のすべての要素を **すべて**最初のものを選択できます。他、 **ノートブック** **ページ**、ノート パソコンと、ページは、対応する要素が選択されている場合にのみ選択できます。
  
```cs
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            ... 
        }

```

**Run**

|||
|:-----|:-----|
|**説明** <br/> |新しいスレッドからクイック ファイリング ダイアログ ボックスが表示されます。ダイアログ ボックスを閉じますを **OnDialogClosed**メソッドが呼び出されます、 **IQuickFilingDialogCallback**インターフェイスへの参照になります。 <br/> |
|**構文** <br/> | `HRESULT Run (`<br/>`[in]IQuickFilingDialogCallback piCallback);` <br/> |
|**パラメーター** <br/> | _piCallback_&ndash;ダイアログボックスが閉じられた後にインスタンス化される**iquickfilingdialogcallback**インターフェイスへの参照。  <br/> |
   
新しいスレッドからクイック ファイリング ダイアログ ボックスを表示、 **Run**メソッドを次のコード例に示します。 
  
```cs
    class OpenQuickFilingDialog
    {
            ... 
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            ... 
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            ... 
        }
    }

```

**TreeCollapsedState**

|||
|:-----|:-----|
|**説明** <br/> |階層ツリーを展開または縮小する必要があるかどうかを示します。  <br/> |
|**構文** <br/> | `HRESULT TreeCollapsedState(`<br/>`[in] TreeCollapsedStateType tcs);` <br/> |
|**パラメーター** <br/> | _tcs_では、ツリーを展開するか、折りたたまれているかどうかを指定します。  <br/> |
   
**NotebookFilterOut**

|||
|:-----|:-----|
|**説明** <br/> |ノート パソコンの種類別に表示の一覧をフィルター処理します。  <br/> |
|**構文** <br/> | `HRESULT NotebookFilterOut(`<br/>`[in] NotebookFilterOutType nfo);` <br/> |
|**パラメーター** <br/> | _nfo_ - は、ボックスの一覧からフィルターを適用するのには、ノートブックのセットを指定します。  <br/> |
   
**ShowCreateNewNotebook**

|||
|:-----|:-----|
|**説明** <br/> |新規のノートブックの作成] ダイアログ ボックスを表示します。  <br/> |
|**構文** <br/> | `HRESULT ShowCreateNewNotebook ();` <br/> |
|**パラメーター** <br/> |なし  <br/> |
   
**addinitialeditor**

|||
|:-----|:-----|
|**説明** <br/> |クイック ファイリング] ダイアログ ボックスで、ノートを初期のエディターとしてユーザーを追加します。  <br/> |
|**構文** <br/> | `HRESULT AddInitialEditor (BSTR initialEditor);` <br/> |
|**パラメーター** <br/> | _initialEditor_のノートブックには、エディターとして追加するユーザーの電子メール アドレス。クイック ファイリング] ダイアログ ボックスを使用してノートブックを作成するときに初期のすべてのエディターで自動的に共有されます。 <br/> |
   
**clearinitialeditors**

|||
|:-----|:-----|
|**説明** <br/> |クイック ファイリング ダイアログ ボックスからすべての最初のエディターを削除します。  <br/> |
|**構文** <br/> | `HRESULT ClearInitialEditors ();` <br/> |
|**パラメーター** <br/> |なし  <br/> |
   
**showsharinghyperlink**

|||
|:-----|:-----|
|**説明** <br/> |クイック ファイリング] ダイアログ ボックスで、共有のヘルプ ハイパーリンクが表示されます。  <br/> |
|**構文** <br/> | `HRESULT ShowSharingHyperlink();` <br/> |
|**パラメーター** <br/> |なし  <br/> |
   
## <a name="iquickfilingdialogcallback-interface"></a>iquickfilingdialogcallback インターフェイス
<a name="odc_IQuickFilingDialog"> </a>

このインターフェイス、ダイアログ ボックスを閉じた後、ダイアログ ボックスのプロパティにアクセスすることができます。OneNote 2013は、ダイアログ ボックスを閉じると、このインターフェイスの **IQuickFilingDialogCallback.OnDialogClose**メソッドを呼び出します。 
  
このインターフェイスを継承するクラスを定義するのには。
  
### <a name="methods"></a>メソッド

次のセクションは以前詳細なインターフェイスに関連付けられたメソッドについて説明します。
  
**ondialogclosed**

|||
|:-----|:-----|
|**説明** <br/> |キャプチャ] ダイアログ ボックスで、ユーザーの選択を使用して機能を追加することができます。クイック ファイリング] ダイアログ ボックスを閉じた後に、このメソッドは呼び出されます。このメソッドは、 **IQuickFilingDialogCallback**インタ フェースを定義する必要がある関数です。 <br/> |
|**構文** <br/> | `HRESULT OnDialogClosed (`<br/>`[in]IQuickFilingDialog dialog);` <br/> |
|**パラメーター** <br/> | _ダイアログ_&ndash; **ondialogclose**メソッドを呼び出した**iquickfilingdialog**オブジェクト。  <br/> |
   
次の使用例は、サンプルの **IQuickFilingDialogCallback**インターフェイスです。 **OnDialogClose**メソッドは、ユーザーの選択クイック ファイリング] ダイアログ ボックスでコンソールに出力します。 
  
```cs
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }

```

## <a name="example"></a>例
<a name="odc_IQuickFilingDialog"> </a>

次のコード例では、カスタマイズされたタイトル、説明、最近の結果のリスト、ツリーの深さ、] チェック ボックスおよびボタンは、クイック ファイリング ダイアログ ボックスを開きます。ユーザーのボタンを押して、項目を選択して、ダイアログ ボックスを閉じると、コンソール ウィンドウでチェック ボックスの状態が表示されます。有効になっているページのボタンを表示するには、ユーザーはツリーの深さはのセクションに設定されているため、ページを検索し、選択する必要があります。ダイアログ ボックスは任意のウィンドウの子ウィンドウです。
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using Microsoft.Office.Interop.OneNote;
namespace SampleQFD
{
    class OpenQuickFilingDialog
    {
        private static EventWaitHandle wh = new AutoResetEvent(false);
        private static IQuickFilingDialog qfDialog;
        private static String strTitle = "Sample Title";
        private static String strDescription = "Sample Description";
        private static String strCheckboxText = "Sample Checkbox";
        static void Main(string[] args)
        {
            Microsoft.Office.Interop.OneNote.Application app = 
                new Microsoft.Office.Interop.OneNote.Application();
            // Instantiate Quick Filing UI
            qfDialog = app.QuickFiling();
            #region//SET API PARAMETERS
            // TITLE
            qfDialog.Title = strTitle;
            // DESCRIPTION
            qfDialog.Description = strDescription;
            // RECENT RESULTS
            qfDialog.SetRecentResults(RecentResultType.rrtFiling,
                /*Current Section*/ true,
                /*Current Page*/ true,
                /*Unfiled Notes*/ true);
            // TREE DEPTH
            qfDialog.TreeDepth = HierarchyElement.heSections;
            // CHECKBOX
            qfDialog.CheckboxText = strCheckboxText;
            qfDialog.CheckboxState = false;
            // BUTTONS
            HierarchyElement heAll = (HierarchyElement) 
                ((uint)HierarchyElement.heNotebooks | 
                (uint)HierarchyElement.heSectionGroups | 
                (uint)HierarchyElement.heSections |  
                (uint)HierarchyElement.hePages);
            
            qfDialog.AddButton("All", heAll, heAll, true);
            qfDialog.AddButton("Notebooks", HierarchyElement.heNotebooks, 
                HierarchyElement.heNotebooks, false);
            qfDialog.AddButton("Pages", HierarchyElement.hePages, 
                HierarchyElement.hePages, false);
            // PARENTWINDOW
            #endregion
            // Display Quick Filing UI
            qfDialog.Run(new Callback());
            // Clean up and Wait so console window does not close
            qfDialog = null;
            wh.WaitOne();
        }
    }
    class Callback : IQuickFilingDialogCallback
    {
        public Callback(){}
        public void OnDialogClosed(IQuickFilingDialog qfDialog)
        {
            Console.WriteLine(qfDialog.SelectedItem);
            Console.WriteLine(qfDialog.PressedButton);
            Console.WriteLine(qfDialog.CheckboxState);
        }
    }
}

```

## <a name="see-also"></a>関連項目

- [OneNote の開発者用リファレンス](onenote-developer-reference.md)


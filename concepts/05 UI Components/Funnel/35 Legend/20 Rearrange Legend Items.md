Although the legend's layout is virtually universal, in some cases, you may need to slightly adjust it, for example, rearrange legend items. You can learn how to do it from the following instructions.

- **Choose legend orientation**        
Depending on whether the legend is oriented vertically or horizontally, the Funnel arranges legend items in columns or in rows. To change the legend orientation, use the [orientation](/api-reference/10%20UI%20Components/BaseLegend/orientation.md '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/legend/#orientation') property.

    ---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#funnelContainer").dxFunnel({
            // ...
            legend: {
                orientation: "vertical" // or "horizontal"
            }
        });
    });

##### Angular

    <!--HTML--><dx-funnel ...>
        <dxo-legend
            orientation="vertical"> <!-- or "horizontal" -->
        </dxo-legend>
    </dx-funnel>

    <!--TypeScript-->
    import { DxFunnelModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxFunnelModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxFunnel ... >
            <DxLegend
                orientation="vertical" <!-- or "horizontal" -->
            />
        </DxFunnel>
    </template>

    <script>
    import DxFunnel, { DxLegend } from 'devextreme-vue/funnel';

    export default {
        components: {
            DxFunnel,
            DxLegend
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Funnel, { Legend } from 'devextreme-react/funnel';

    class App extends React.Component {
        render() {
            return (
                <Funnel ... >
                    <Legend
                        orientation="vertical" {/* or "horizontal" */}
                    />
                </Funnel>
            );
        }
    }

    export default App;

---

    [note] To center a horizontally-oriented legend, assign *"center"* to the [horizontalAlignment](/api-reference/10%20UI%20Components/BaseLegend/horizontalAlignment.md '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/legend/#horizontalAlignment') property. For details on the legend's location, refer to the [Relocate the Legend](/concepts/05%20UI%20Components/Funnel/35%20Legend/10%20Relocate%20the%20Legend.md '/Documentation/Guide/UI_Components/Funnel/Legend/Relocate_the_Legend/') topic.

- **Set the number of columns or rows**     
To distribute all legend items between several columns (in a vertically-oriented legend) or rows (in a horizontally-oriented legend), set the [columnCount](/api-reference/10%20UI%20Components/BaseLegend/columnCount.md '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/legend/#columnCount') or [rowCount](/api-reference/10%20UI%20Components/BaseLegend/rowCount.md '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/legend/#rowCount') property respectively.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#funnelContainer").dxFunnel({
            // ...
            legend: {
                // ...
                columnCount: 3
                // rowCount: 2
            }
        });
    });

##### Angular

    <!--HTML--><dx-funnel ...>
        <dxo-legend ...
            [columnCount]="3">
            <!-- [rowCount]="2"> -->
        </dxo-legend>
    </dx-funnel>

    <!--TypeScript-->
    import { DxFunnelModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxFunnelModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxFunnel ... >
            <DxLegend
                :column-count="3" 
                <!-- :row-count="2" -->
            />
        </DxFunnel>
    </template>

    <script>
    import DxFunnel, { DxLegend } from 'devextreme-vue/funnel';

    export default {
        components: {
            DxFunnel,
            DxLegend
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Funnel, { Legend } from 'devextreme-react/funnel';

    class App extends React.Component {
        render() {
            return (
                <Funnel ... >
                    <Legend
                        columnCount={3} 
                        {/* rowCount={2} */}
                    />
                </Funnel>
            );
        }
    }

    export default App;

---

- **Adjust the empty space between columns and rows**         
Regardless of the legend orientation, you can adjust the empty space between columns and rows using the [columnItemSpacing](/api-reference/10%20UI%20Components/BaseLegend/columnItemSpacing.md '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/legend/#columnItemSpacing') and [rowItemSpacing](/api-reference/10%20UI%20Components/BaseLegend/rowItemSpacing.md '/Documentation/ApiReference/UI_Components/dxFunnel/Configuration/legend/#rowItemSpacing') properties respectively.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#funnelContainer").dxFunnel({
            // ...
            legend: {
                // ...
                columnItemSpacing: 20,
                rowItemSpacing: 30
            }
        });
    });

##### Angular

    <!--HTML--><dx-funnel ...>
        <dxo-legend ...
            [columnItemSpacing]="20"
            [rowItemSpacing]="30">
        </dxo-legend>
    </dx-funnel>

    <!--TypeScript-->
    import { DxFunnelModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxFunnelModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxFunnel ... >
            <DxLegend ...
                :column-item-spacing="20"
                :row-item-spacing="30"
            />
        </DxFunnel>
    </template>

    <script>
    import DxFunnel, { DxLegend } from 'devextreme-vue/funnel';

    export default {
        components: {
            DxFunnel,
            DxLegend
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Funnel, { Legend } from 'devextreme-react/funnel';

    class App extends React.Component {
        render() {
            return (
                <Funnel ... >
                    <Legend
                        columnItemSpacing={20}
                        rowItemSpacing={30}
                    />
                </Funnel>
            );
        }
    }

    export default App;

---

Below, you can try out all the mentioned properties in action.

<div class="simulator-desktop-container" data-view="/Content/Applications/21_2/DataVisualization/Guides/FunnelLegend/rearrangeLegendItems.html, /Content/Applications/21_2/DataVisualization/Guides/FunnelLegend/rearrangeLegendItems.js, /Content/Applications/21_2/DataVisualization/Guides/FunnelLegend/rearrangeLegendItems.css"></div>

#####See Also#####
- [Relocate the Legend](/concepts/05%20UI%20Components/Funnel/35%20Legend/10%20Relocate%20the%20Legend.md '/Documentation/Guide/UI_Components/Funnel/Legend/Relocate_the_Legend/')
- [Funnel Demos](https://js.devexpress.com/Demos/WidgetsGallery/Demo/Charts/FunnelChart)

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Taxonomy Tree</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/d3/7.8.5/d3.min.js"></script>
    <style>
        body {
            margin: 0;
            padding: 20px;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .container {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        h1 {
            text-align: center;
            color: #2c3e50;
            margin-bottom: 30px;
            font-size: 2.5em;
            font-weight: 300;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        #tree-container {
            width: 100%;
            height: 800px;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: inset 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .node circle {
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .node text {
            font: 14px 'Segoe UI', sans-serif;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .node:hover circle {
            stroke-width: 3px;
            filter: drop-shadow(0 0 8px rgba(0, 0, 0, 0.3));
        }

        .node:hover text {
            font-weight: bold;
            font-size: 16px;
        }

        .link {
            fill: none;
            stroke-width: 2px;
            transition: all 0.3s ease;
        }

        .link:hover {
            stroke-width: 4px;
            filter: drop-shadow(0 0 6px rgba(0, 0, 0, 0.3));
        }

        .root-node circle {
            fill: #e74c3c;
            stroke: #c0392b;
        }

        .category-node circle {
            fill: #3498db;
            stroke: #2980b9;
        }

        .leaf-node circle {
            fill: #27ae60;
            stroke: #229954;
        }

        .root-link {
            stroke: #e74c3c;
        }

        .category-link {
            stroke: #3498db;
        }

        .leaf-link {
            stroke: #27ae60;
        }

        .tooltip {
            position: absolute;
            background: rgba(0, 0, 0, 0.9);
            color: white;
            padding: 10px 15px;
            border-radius: 8px;
            font-size: 12px;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: 1000;
            backdrop-filter: blur(5px);
        }

        .controls {
            text-align: center;
            margin-top: 20px;
        }

        .control-button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            padding: 10px 20px;
            margin: 0 10px;
            border-radius: 25px;
            cursor: pointer;
            font-size: 14px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .control-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
        }

        .legend {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 14px;
            color: #2c3e50;
        }

        .legend-circle {
            width: 16px;
            height: 16px;
            border-radius: 50%;
            border: 2px solid;
        }

        @media (max-width: 768px) {
            .container {
                padding: 20px;
                margin: 10px;
            }
            
            h1 {
                font-size: 2em;
            }
            
            #tree-container {
                height: 600px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Privacy Taxonomy Tree</h1>
        <div id="tree-container"></div>
        <div class="controls">
            <button class="control-button" onclick="expandAll()">Expand All</button>
            <button class="control-button" onclick="collapseAll()">Collapse All</button>
            <button class="control-button" onclick="resetView()">Reset View</button>
        </div>
        <div class="legend">
            <div class="legend-item">
                <div class="legend-circle" style="background: #e74c3c; border-color: #c0392b;"></div>
                <span>Root Concept</span>
            </div>
            <div class="legend-item">
                <div class="legend-circle" style="background: #3498db; border-color: #2980b9;"></div>
                <span>Main Categories</span>
            </div>
            <div class="legend-item">
                <div class="legend-circle" style="background: #27ae60; border-color: #229954;"></div>
                <span>Techniques & Methods</span>
            </div>
        </div>
    </div>

    <div class="tooltip" id="tooltip"></div>

    <script>
        // Data structure for the privacy tree
        const treeData = {
            name: "Privacy",
            children: [
                {
                    name: "Anonymity",
                    children: [
                        { name: "Identity" },
                        { name: "Claims" },
                        { name: "Anonymous Credentials" },
                        { name: "Identity Mixers" },
                        { name: "Mixnets" },
                        { name: "Group Signatures" },
                        { name: "Ring Signatures" },
                        { name: "CoinJoin + CoinShuffle" },
                        { name: "Blind Signatures" },
                        { name: "Bulletproofs" },
                        { name: "BOLT" },
                        { name: "Monero, Zcash" },
                        { name: "Stealth Transactions" }
                    ]
                },
                {
                    name: "Confidentiality",
                    children: [
                        { name: "Credentials" },
                        { name: "PKI" },
                        { name: "Private Key Infrastructure" },
                        { name: "Digital Signature" },
                        { name: "Project" },
                        { name: "ZK-SNARKs" },
                        { name: "ZK-STARKs" },
                        { name: "ZK-Rollups" },
                        { name: "PGP" },
                        { name: "PRF" },
                        { name: "HMAC, KDF" },
                        { name: "OPRF" },
                        { name: "Homomorphic Encryption (24)" },
                        { name: "PKE, FHE, SMC" }
                    ]
                }
            ]
        };

        // Set up dimensions and margins
        const margin = { top: 40, right: 90, bottom: 40, left: 90 };
        const width = 960 - margin.left - margin.right;
        const height = 720 - margin.top - margin.bottom;

        // Create SVG
        const svg = d3.select("#tree-container")
            .append("svg")
            .attr("width", width + margin.left + margin.right)
            .attr("height", height + margin.top + margin.bottom)
            .style("background", "linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%)");

        const g = svg.append("g")
            .attr("transform", `translate(${margin.left},${margin.top})`);

        // Create tree layout
        const tree = d3.tree().size([height, width]);

        // Create hierarchy
        const root = d3.hierarchy(treeData);
        
        let i = 0;
        const duration = 750;

        // Assign unique IDs and initialize
        root.x0 = height / 2;
        root.y0 = 0;

        // Collapse all children initially except first level
        root.children.forEach(collapse);

        function collapse(d) {
            if (d.children) {
                d._children = d.children;
                d._children.forEach(collapse);
                d.children = null;
            }
        }

        // Tooltip
        const tooltip = d3.select("#tooltip");

        // Update function
        function update(source) {
            const treeData = tree(root);
            const nodes = treeData.descendants();
            const links = treeData.descendants().slice(1);

            // Normalize for fixed-depth
            nodes.forEach(d => d.y = d.depth * 200);

            // Update nodes
            const node = g.selectAll('g.node')
                .data(nodes, d => d.id || (d.id = ++i));

            // Enter new nodes
            const nodeEnter = node.enter().append('g')
                .attr('class', 'node')
                .attr('transform', d => `translate(${source.y0},${source.x0})`)
                .on('click', click)
                .on('mouseover', function(event, d) {
                    const descriptions = {
                        "Privacy": "The overarching concept of protecting personal information and maintaining control over data",
                        "Anonymity": "Techniques that hide the identity of users while allowing them to interact",
                        "Confidentiality": "Methods that protect the content and meaning of data from unauthorized access",
                        "ZK-SNARKs": "Zero-Knowledge Succinct Non-Interactive Arguments of Knowledge",
                        "ZK-STARKs": "Zero-Knowledge Scalable Transparent Arguments of Knowledge",
                        "Mixnets": "Networks that hide communication patterns by mixing messages",
                        "Ring Signatures": "Signatures that prove membership in a group without revealing which member signed",
                        "Homomorphic Encryption (24)": "Encryption allowing computation on encrypted data without decryption"
                    };
                    
                    const description = descriptions[d.data.name] || `Privacy technique: ${d.data.name}`;
                    
                    tooltip
                        .style("opacity", 1)
                        .style("left", (event.pageX + 10) + "px")
                        .style("top", (event.pageY - 10) + "px")
                        .html(description);
                })
                .on('mouseout', function() {
                    tooltip.style("opacity", 0);
                });

            // Add circles
            nodeEnter.append('circle')
                .attr('r', 1e-6)
                .attr('class', d => {
                    if (d.depth === 0) return 'root-node';
                    if (d.depth === 1) return 'category-node';
                    return 'leaf-node';
                })
                .style('stroke-width', '2px');

            // Add text
            nodeEnter.append('text')
                .attr('dy', '.35em')
                .attr('x', d => d.children || d._children ? -13 : 13)
                .attr('text-anchor', d => d.children || d._children ? 'end' : 'start')
                .text(d => d.data.name)
                .style('fill-opacity', 1e-6);

            // Transition nodes to their new position
            const nodeUpdate = nodeEnter.merge(node);

            nodeUpdate.transition()
                .duration(duration)
                .attr('transform', d => `translate(${d.y},${d.x})`);

            nodeUpdate.select('circle')
                .transition()
                .duration(duration)
                .attr('r', d => {
                    if (d.depth === 0) return 12;
                    if (d.depth === 1) return 10;
                    return 8;
                });

            nodeUpdate.select('text')
                .transition()
                .duration(duration)
                .style('fill-opacity', 1);

            // Remove exiting nodes
            const nodeExit = node.exit().transition()
                .duration(duration)
                .attr('transform', d => `translate(${source.y},${source.x})`)
                .remove();

            nodeExit.select('circle')
                .attr('r', 1e-6);

            nodeExit.select('text')
                .style('fill-opacity', 1e-6);

            // Update links
            const link = g.selectAll('path.link')
                .data(links, d => d.id);

            // Enter new links
            const linkEnter = link.enter().insert('path', 'g')
                .attr('class', 'link')
                .attr('d', d => {
                    const o = { x: source.x0, y: source.y0 };
                    return diagonal(o, o);
                })
                .attr('class', d => {
                    if (d.parent && d.parent.depth === 0) return 'link category-link';
                    if (d.parent && d.parent.depth === 1) return 'link leaf-link';
                    return 'link root-link';
                });

            // Transition links to their new position
            const linkUpdate = linkEnter.merge(link);

            linkUpdate.transition()
                .duration(duration)
                .attr('d', d => diagonal(d, d.parent));

            // Remove exiting links
            link.exit().transition()
                .duration(duration)
                .attr('d', d => {
                    const o = { x: source.x, y: source.y };
                    return diagonal(o, o);
                })
                .remove();

            // Store old positions for transition
            nodes.forEach(d => {
                d.x0 = d.x;
                d.y0 = d.y;
            });
        }

        // Diagonal path function
        function diagonal(s, d) {
            return `M ${s.y} ${s.x}
                    C ${(s.y + d.y) / 2} ${s.x},
                      ${(s.y + d.y) / 2} ${d.x},
                      ${d.y} ${d.x}`;
        }

        // Click handler
        function click(event, d) {
            if (d.children) {
                d._children = d.children;
                d.children = null;
            } else {
                d.children = d._children;
                d._children = null;
            }
            update(d);
        }

        // Control functions
        function expandAll() {
            function expand(d) {
                if (d._children) {
                    d.children = d._children;
                    d._children = null;
                }
                if (d.children) d.children.forEach(expand);
            }
            expand(root);
            update(root);
        }

        function collapseAll() {
            function collapse(d) {
                if (d.children) {
                    d._children = d.children;
                    d._children.forEach(collapse);
                    d.children = null;
                }
            }
            root.children.forEach(collapse);
            update(root);
        }

        function resetView() {
            collapseAll();
            // Expand only first level
            if (root._children) {
                root.children = root._children;
                root._children = null;
            }
            update(root);
        }

        // Initial render
        update(root);

        // Add some initial animation
        setTimeout(() => {
            if (root._children) {
                root.children = root._children;
                root._children = null;
            }
            update(root);
        }, 500);
    </script>
</body>
</html>

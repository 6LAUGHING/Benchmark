void input()   
{	
	int i;
	cout << "Input the number of flow ports、mixers、heater、filter、detector、separator、and components"<< endl;
	cin >> maxPort >> maxMixer >> maxHeater >> maxFilter >> maxDetector >> maxSeparator >> deviceNum;
   	cout << "Input the number of operations and edges in a sequencing graph" << endl;
	cin >> N >> M;
	cout << "Input the type of each operation（1: mix, 2: heat, 3: filter, 4: detect, 5: separate)" << endl;
	for (i = 1; i <= N; i++)
	{
	      cin >> op[i].op_type;
	}
	
	cout << "Input the duration time of each operation" << endl;
	for (i = 1; i <= N; i++)
	{
	      cin >> op[i].runTime;
	}
	
	cout<<"Input the bound component of each operation"<<endl;
	for(i = 1; i <= N; i++)
	{
	      cin >> op[i].bind_Id;
	}
	cout << "Input each edge in sequencing graph and the bound fluidic ports" << endl;
	int a, b,in_port,out_port;
	while (M--)
	{
	      cin >> a >> b >> in_port >>out_port;
	}
	cout << "Input the flow-layer chip layout" <<endl;
                 cout << "Input the number of  nodes and edges contained in a chip layout" <<endl;
                 cin >> Nodenum >> edgenum ;	
	cout << "Input the infomation of each noed (node type, x-coordinate, and y-coordinate)" <<endl;
	for(i = 1 ; i <= Nodenum ; i++)
	{
	      cin >> Node[i].Node_type >> Node[i].n_x >> Node[i].n_y;  \\（type：1:input port, 2: output port, 3: mixer, 4: heater, 5: filter, 6: detector, 7: separator, 8: T-intersection, 9: cross intersection）
	}
                 cout << "Input the information of each valve (x-coordinate, y-coordinate, and the node to which the valve belongs)" <<endl;
                 for(i = 1 ; i <= valvecount ; i++)
                 {
                       cin >> v[i].p_x >> v[i].p_y >> v[i].belong_Node;
	}
	cout << "Input the information of each flow channel" <<endl;
	for (i = 1 ; i <= edgenum; i ++)
	{
	       cin >> Edge[i].node1 >> Edge[i].node2 >> Edge[i].v1 >> Edge[i].v2 >> Edge[i].length;
	}
}

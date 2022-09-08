# function_to_remove_element_from_queue




// Function to remove an element from
// the queue
void remove(int t, queue<int>& q)
{

	// Helper queue to store the elements
	// temporarily.
	queue<int> ref;
	int s = q.size();
	int cnt = 0;

	// Finding the value to be removed
	while (q.front() != t and !q.empty()) {
		ref.push(q.front());
		q.pop();
		cnt++;
	}

	// If element is found
	
		q.pop();
		while (!ref.empty()) {

			// Pushing all the elements back into q
			q.push(ref.front());
			ref.pop();
		}
		int k = s - cnt - 1;
		while (k--) {

			// Pushing elements from front of q to its back
			int p = q.front();
			q.pop();
			q.push(p);
		
	}
}
